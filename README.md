# Text sample generator
 Find the smallest collection of words that 
 contains the most letter pair combinations.

This repo has two tools: a `Generator` which creates a lot of data objects and 2 
result paragraphs based on a dictionary,
and a `Paragraph builder` which uses this data to help build custom result paragraphs.

## Generator tool

For a given set of words (dictionary), and a given alphabet (in this case we use basic 
latin lowercase alphabet), there will be some letter pairs from the alphabet 
that never occur in the dictionary. Even within this maximum letter pair coverage per dictionary, 
there are multiple "result" paragraphs that contain all possible letter 
pairs for that dictionary. This tool includes two automatically generated 
result paragraphs per dictionary: one paragraph that favors words with many 
letter pairs ("least words") and one paragraph that favors shorter words ("shortest words").

Here are the links to all the results for every dictionary, in text file format:

| dictionary | source words | result text file | resulting words | unused letter pairs |
| --- | --- | --- | --- | --- |
| **swadesh_207** | 207   | [swadesh_207_result_least_words.txt](swadesh_207/swadesh_207_result_least_words.txt)<br>[swadesh_207_result_shortest_words.txt](swadesh_207/swadesh_207_result_shortest_words.txt) | 102<br>127 | 480 (71%) |
| **english_10** | ~4,000   | [english_10_result_least_words.txt](english_10/english_10_result_least_words.txt)<br>[english_10_result_shortest_words.txt](english_10/english_10_result_shortest_words.txt) | 215<br>331 | 302 (45%)|
| **english_50** | ~17,000  | [english_50_result_least_words.txt](english_50/english_50_result_least_words.txt)<br>[english_50_result_shortest_words.txt](english_50/english_50_result_shortest_words.txt) | 327<br>437 | 158 (23%) |
| **english_70** | ~112,500  | [english_70_result_least_words.txt](english_70/english_70_result_least_words.txt)<br>[english_70_result_shortest_words.txt](english_70/english_70_result_shortest_words.txt) | 388<br>587 | 78 (12%) |
| **english_95** | ~180,000 | [english_95_result_least_words.txt](english_95/english_95_result_least_words.txt)<br>[english_95_result_shortest_words.txt](english_95/english_95_result_shortest_words.txt) | 427<br>589 | 30 (4%) |

As an observation, the larger word sets do result in covering more letter pairs... but these word lists are full of very obscure words. So, more coverage definitely comes at the cost of leveraging words that you've probably never seen before. On the other hand, if you want to make some sort of recognizable paragraph of words, the ultra-low end Swadesh dictionary or English 10 dictionary may be the way to go.

You can email [matt@mattlag.com](matt@mattlag.com) with any questions or comments.

### Results
With the goal of having closely resembling a "normal" paragraph of text with the most 
letter pair coverage, personally I'm going to use the results from the English 10 set. 
Yes, the coverage is less than other results, but starting with the English 50 set, 
the majority of words are just too odd.

**English 10: Least Words**

> establishment accidentally administration afterwards disadvantage ahead straightforward majority mistaking alternatively fundamentally misunderstanding chaos applications broadcasting automatically available withdraw maximum displaying crazy embarrassing rubbish deliberately responsibility objections submitting borrowing observation doubtful contributions obviously thereby communications circumstances characters background conclusion acquiring descriptions electronics introduction consistency recommendation feedback additional knowledge adjust admittedly midnight documentation addressing misunderstands undergraduates hardware everybody disappearing somebody sophisticated guaranteeing definitions registering comprehensive rejecting seeking announcement simultaneously representation consequences interpretation queue nevertheless elsewhere experiencing keyboard facilities professional difficulties significantly reflecting frequently justifying investigate arrangements meaningful suggestions discouraging accordingly algorithms buildings strength terminology beforehand forthcoming thoroughly techniques authorities throughout months hundreds worthwhile philosophy appreciating opportunities likewise mediums fixing bizarre justification packages brackets quickly networks awkward lucky calculations album considerable yourself talking almost development helpful already individuals absolutely themselves always combinations harmful harmless autumn demonstration comparatively mysterious unfortunately unhappy enjoy thinking certainly environment unnecessarily unpleasant unreasonable continuously conventional unwanted anonymous misunderstood whatsoever programmers oh pointless projects looking controlling possibilities potentially improvements boxes destroying dozens updating developing upsetting manipulation upwards occupying disturbing performance perhaps particularly information instruction intervention unnecessary husband successfully asking criticism square answering symbols switching atmosphere output publication excluding sufficiently requirements corrupting buying individually avoiding heavy awful widespread unknown rewrite borrows growth examined exceptions executing complexity extending cycles destroyed style syntax everyone anyplace everything everywhere citizen

**English 10: Shortest Words**

> able act add leaf age ahead aid major make all am an chaos gap are as at cause gave law tax day lazy bad rubber be bid object submit box brand jobs doubt bug obvious by can occur ice char city back club code acquire cry cs cup cycle feedback broadcast edge did adjust badly admit midnight do dry adds due advice hardware body eat debate neck bed see left leg behalf being reject seek cell deem end video deep equal err hes bet queue even few sex eye fan fed off fit fly for fry fun modify meaningful bigger high girl glad sign go grew bugs length gun apology had forthcoming withdraw he hid highly algorithm technical hot three months eight huge worthwhile why via library die if big like ill aim in prior chip unique air is it medium five fix size job jump package key background kid quickly knew asks awkward lucky album welcome old led half lie bulk film log help already also felt blue solve always mad dumb me harmful mix firmly common autumn mod dump aims much my name inch and net info hang unhappy nice enjoy bank only government annoy no input unreasonable runs cent numb invent unwanted any boat lock doe of dog oh oil project book come on too pop or cost got our love how boy dozen pay update pen helpful graph pi plan equipment apple press chips kept put upwards copy quit ran nearby force card re perfect argue perhaps rid dark arm turn row sharp bars art run serve forward sad husband disc satisfy she sit ask slip small so spot square less best sum answer busy catch ate doubtful the tie title treatment to output try its putt tune two luck judge stuff quote up us but buy van vote heavy war we awful who win slowly own write laws growth exact except boxes exist expand next maybe dying style symbol syntax you type buys byte anyway bizarre

## Paragraph builder tool
The Generator creates two flavors of "result paragraphs"... but what if these paragraphs
don't quite meet your expectations? The Paragraph builder tool lets you use data generated 
by the Generator to build a custom paragraph for yourself.

The Paragraph builder has 3 columns:
 1. Pairs checklist - this keeps track of the letter pairs in your paragraph. Either displaying an ❌ if the pair is missing, or displaying a count of how many times that pair occurs.
 2. Word list - these are words from your dictionary, sorted by letter pair. So, each word may show up more than once in the overall list. Each word is a button, and clicking it will add that word to your result paragraph. Each word also has a "word score" number on it. This tells you how many letter pairs this word would cover, if you select it. Every time you add a word, the "word score" for each word is re-calculated.
 3. Result paragraph - this is where your result is displayed. It also has buttons for every word, clicking these will remove that word from your result paragraph.

The overall process is just scrolling through the word list, and choosing what words you 
want to add to your paragraph... based on whatever criteria you want.

**NOTE** The Paragraph Builder tool uses the `English 10` dictionary. Also included in the 
html file is the `English 50` dictionary: you will have to edit the html file to disable 
one dictionary and enable the other. Overall, this tool is *very* slow. The `English 10` 
dictionary is small, and even it is slow. the `English 50` dictionary will take many 
seconds after each click on fast computers. This is why the tool does not include any 
of the larger dictionaries and just defaults to the small one.


# Fun facts
Hopefully the results will be useful, but there are also some results that are just interesting. Here are a few:

**Letter combinations that were not found in the English 95 set (about 180,000 words):**

> cj fq gx hx jf jq jw jx jz qb qc qj qk qm qv qx qy qz sx vb vg vj vq vx wx xj xk zj zq zx


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

**The ten most common two-letter pairs, based on how many words contain them in the English 95 set:**
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
spacing between letters, etc... A good set of test text will either confirm 
a typeface works well, or highlights issues to be addressed.

## How?
Given some dictionary of words, we'll brute force look for pairs of letters, 
and as a second step, be able to assemble paragraphs of text that 
contains as many of the letter pairs as possible.

## Source
Word lists will be pulled from SCOWL ([wordlist.aspell.net](http://wordlist.aspell.net/)), which is:
  
> SCOWL (Spell Checker Oriented Word Lists) and Friends is a database of information on English 
> words useful for creating high-quality word lists suitable for use in spell checkers of most 
> dialects of English.

These word lists are divided into categories that correspond to length. Sub-directories in this 
project are named to correspond to these, for example: `english_10`, `english_50`, `english_70`, 
and `english_95`.