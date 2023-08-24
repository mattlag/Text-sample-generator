# Text sample generator
 Find the shortest test string that contains the most letter combinations.

If you are just interested in the result (aka the shortest overall collection of words with the most letter-pair coverage) then here are links to the result files:

| dictionary | source words | result text file | resulting words | unused letter pairs |
| --- | --- | --- | --- | --- |
| **english_10** | ~4,000  | [english_10_result.txt](english_10/english_10_result.txt) | 374 | 302 |
| **english_50** | ~17,000 | [english_50_result.txt](english_50/english_50_result.txt) | 518 | 158 |
| **english_95** | unknown | _not yet generated_ | | |

You can email [matt@mattlag.com](matt@mattlag.com) with any questions or comments.
# More info
## Why?
For testing new typefaces, it's good to have example text that surfaces how
that text performs. Mostly this concerns letter line weights, negative space,
spacing between letters, etc... A good set of test strings will either confirm 
a typeface works well, or highlights issues to be addressed.

## How?
Given some dictionary of words, we'll brute force look for pairs of letters, 
and as a second step, be able to assemble a paragraph of text that 
contains as many of the letter pairs as possible in the shortest overall length.

## Source
Word lists will be pulled from SCOWL ([wordlist.aspell.net](http://wordlist.aspell.net/)), which is:
  
	SCOWL (Spell Checker Oriented Word Lists) and Friends is a database of information on English words useful for creating high-quality word lists suitable for use in spell checkers of most dialects of English.

These word lists are divided into categories that correspond to length. Sub-directories in this project are named to correspond to these, for example: `english_10`, `english_50`, and `english_95`.

