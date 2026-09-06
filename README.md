<H3>ENTER YOUR NAME V RAKSHITA</H3>
<H3>ENTER YOUR REGISTER NO.212224100049 </H3>
<H3>EX. NO.6</H3>
<H3>DATE:</H3>
<H1 ALIGN =CENTER>Implementation of Semantic ANalysis</H1>
<H3>Aim: to perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques. </H3> 
 <BR>
<h3>Algorithm:</h3>
Step 1: Import the nltk library.<br>
Step 2: Download the 'punkt', 'wordnet', and 'averaged_perceptron_tagger' resources.<br>
Step 3:Accept user input for the text.<br>
Step 4:Tokenize the input text into words using the word_tokenize function.<br>
Step 5:Iterate through each word in the tokenized text.<br>
•	Perform part-of-speech tagging on the tokenized words using nltk.pos_tag.<br>
•	Print each word along with its corresponding part-of-speech tag.<br>
•	For each verb , iterate through its synsets (sets of synonyms) using wordnet.synsets(word).<br>
•	Extract synonyms and antonyms using lemma.name() and lemma.antonyms()[0].name() respectively.<br>
•	Print the unique sets of synonyms and antonyms.
<H3>Program:</H3>

```python
import nltk
#import wordnet
nltk.download( 'punkt_tab' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger_eng' )
sentence=input ()
# Print the parts of speech
for word, tag in pos_tags:
    print(word, tag)
# Tokenize the sentence into words
words = word_tokenize(sentence)
# Identify the parts of speech for each word
pos_tags= nltk.pos_tag(words)
from nltk.corpus import wordnet

# Identify synonyms and antonyms for each word
synonyms =[]
antonyms =[]
for word in words:
	for syn in wordnet.synsets(word) :
		for lemma in syn.lemmas():
			synonyms . append (lemma . name( ) )
			if lemma . antonyms():
				antonyms . append ( lemma. antonyms ( ) [0] . name ( ) )
# Print the synonyms and antonyms
print ( "Synonyms : " ,set (synonyms) )
print ( "Antonyms : " ,set(antonyms) )
```
<H3>Output</H3>
input sentence: 

<img width="384" height="42" alt="image" src="https://github.com/user-
 attachments/assets/27d99ea8-1a8e-4cb4-81be-57937c11c3e6" />

 <img width="140" height="205" alt="image" src="https://github.com/user-attachments/assets/1329b558-a16f-41b9-9715-1bb221d8650b" />

```
Synonyms :  {'faineant', 'work-shy', 'dodger', 'weenie', 'tail', 'fob', 'all_over', 'click', 'rise', 'discombobulate', 'play_a_trick_on', 'wienerwurst', 'tag', 'otiose', 'complete', 'stand_out', 'terminated', 'leap_out', 'go_after', 'play_a_joke_on', 'heel', 'firedog', 'jump', 'alternate', 'lazy', 'andiron', 'climb_up', 'play_tricks', 'cad', 'trail', 'confuse', 'start', 'track', 'skip', 'concluded', 'pass_over', 'slothful', 'trick', 'derail', 'jumpstart', 'spring', 'slyboots', 'bedevil', 'fox', 'saltation', 'ended', 'blackguard', 'hotdog', 'skip_over', 'confound', 'frank', 'dog-iron', 'frump', 'domestic_dog', 'indolent', 'bounder', 'pull_a_fast_one_on', 'frankfurter', 'parachute', 'hound', 'chase', 'hot_dog', 'chute', 'parachuting', 'befuddle', 'detent', 'Fox', "o'er", 'dog', 'bound', 'throw', 'stick_out', 'Charles_James_Fox', 'pawl', 'jump-start', 'give_chase', 'leap', 'jump_off', 'over', 'wiener', 'jumping', 'Canis_familiaris', 'startle', 'chase_after', 'jump_out', 'George_Fox', 'flim-flam', 'fuddle'}
Antonyms :  set()
```
 



<H3>Result:</H3>
Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.
