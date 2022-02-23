# Solver for TwentyLetters.com
by Trey Reynolds 02/22/22

Steps:

1. Download the Scrabble dictionary from some random github repo.
2. Pre-compute a sorted word data structure.
  * Pre-sorting the dictionary only happens once.
  * This gives a 2x-5x speed increase in the worst case search.
3. Compute the full list of all possible words sorted by score.
4. Recursively do the same procedure with remaining letters until either:
  * There are no remaining letters.
  * No words are found with the remaining letters.
5. If the recursion base case is met back up and try the next "final word".
  * There is a specified search depth of words per "level".
  * The default depth is 30 words.
6. Keep doing this until you run out of words, print only the best results.

