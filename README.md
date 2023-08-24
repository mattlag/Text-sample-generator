# Text sample generator
 Find the smallest collection of words that contains the most letter pair combinations.

If you are just interested in the result (aka the shortest overall collection of words with the most letter-pair coverage) then here are links to the result files:

| dictionary | source words | result text file | resulting words | unused letter pairs |
| --- | --- | --- | --- | --- |
| **swadesh_207** | 207   | [swadesh_207_result.txt](swadesh_207/swadesh_207_result.txt) | 195 | 480 |
| **english_10** | ~4,000   | [english_10_result.txt](english_10/english_10_result.txt) | 373 | 302 |
| **english_50** | ~17,000  | [english_50_result.txt](english_50/english_50_result.txt) | 517 | 158 |
| **english_95** | ~180,000 | [english_95_result.txt](english_95/english_95_result.txt) | 645 | 30  |

As an observation, the larger word sets do result in covering more letter pairs... but these word lists are full of very obscure words. So, more coverage definitely comes at the cost of leveraging words that you've probably never seen before. On the other hand, if you want to make some sort of recognizable paragraph of words, the ultra-low end Swadesh dictionary or English 10 dictionary may be the way to go.

You can email [matt@mattlag.com](matt@mattlag.com) with any questions or comments.

# Fun facts
Hopefully the results will be useful, but there are also some results that are just interesting. Here are a few:

**Letter combinations that were not found in the English 95 set (about 180,000 words):**
```
cj fq gx hx jf jq jw jx jz qb qc qj qk qm qv qx qy qz sx vb vg vj vq vx wx xj xk zj zq zx
```

**Letter combinations that only occur once in the English 95 set:**
  - `cx` from "acxoyatl"
  - `fv` from "arfvedsonites"
  - `gq` from "negqtiator"
  - `jg` from "jger"
  - `jv` from "blijver"
  - `kq` from "cuckquean"
  - `kx` from "kickxia"
  - `kz` from "malikzadi"
  - `mq` from "circumquaque"
  - `px` from "apx"
  - `qg` from "penetrolqgy"
  - `ql` from "taqlid"
  - `qn` from "hlqn"
  - `qo` from "yaqonas"
  - `vf` from "vfw"
  - `vh` from "jhvh"
  - `vz` from "shivzoku"
  - `yj` from "freyja"

**The ten most common two-letter pair, based on how many words contain them in the English 95 set:**
1.  er
2.  in
3.  on
4.  ti
5.  te
6.  es
7.  an
8.  al
9.  at
10. en

Hopefully that was interesting - possibly useful for word games?

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
  
> SCOWL (Spell Checker Oriented Word Lists) and Friends is a database of information on English words useful for creating high-quality word lists suitable for use in spell checkers of most dialects of English.

These word lists are divided into categories that correspond to length. Sub-directories in this project are named to correspond to these, for example: `english_10`, `english_50`, and `english_95`.

