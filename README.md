<H3>NAME: SUJITHRA B K N</H3>
<H3>REGISTER NO: 212222230153</H3>
<H3>EX. NO:6</H3>
<H3>DATE:</H3>
<H1 ALIGN =CENTER>Implementation of Semantic ANalysis</H1>
<H3>Aim: </H3> 
 To perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques. 
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

```
import nltk
#import wordnet
nltk.download( 'punkt' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger' )
sentence=input()
# Tokenize the sentence into words
words = word_tokenize(sentence)
# Identify the parts of speech for each word
pos_tags= nltk.pos_tag(words)
# Print the parts of speech
for word, tag in pos_tags:
	print(word,"-",tag)
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

<H3>Output:</H3>

i.) Sample Input

![Screenshot 2024-04-27 114409](https://github.com/sujithrabkn/Ex-6--AAI/assets/119477857/78e5a80e-d5e1-4240-8bc5-e38c0dcaae70)

ii.) Sample Output

![Screenshot 2024-04-27 114113](https://github.com/sujithrabkn/Ex-6--AAI/assets/119477857/b47804e4-ef53-4306-8b4c-380e38a7d533)


![Screenshot 2024-04-27 114151](https://github.com/sujithrabkn/Ex-6--AAI/assets/119477857/498993bc-574b-4827-9b0d-cf4fc798b2ed)

<H3>Result:</H3>
Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.
