# Cyber_Bullying_Detection

![image](https://user-images.githubusercontent.com/99632495/236155204-977dc251-78df-42aa-b24a-708d7b710095.png)
## A.  Data Collection
We have used Dataturks’ Tweet Dataset for Cybertroll
Detection obtained from Kaggle [1] for reaching the
final results. Because of the seriousness of the issue
we aim to resolve, it was crucial to choose a dataset
that was complete, reliable, relevant, and to the point.
While we considered many other datasets as well, many
of them either had missing attributes, were too low
in quality, or were found to have irrelevant data after
manual inspection. Thus, after having tried out of many
other open sourced datasets, we came down to [1] as it
seemed in line with all the parameters required.
Here is the Detailed Description of the dataset:
1) It is a partially manually labelled dataset.
2) Total Instances: 20001
The dataset has 2 attributes- tweet and label [0 corresponds to No while 1 corresponds to Yes]

## B. Data Preprocessing
The preprocessing steps were done as follows using
the nltk library along with regex:
1) Word Tokenization: A Token is a single entity that
is building blocks for sentence or paragraph. Word
Tokenization converts our text to separate words in
a list.
2) Stop words filtering is done using
nltk.corpus.stopwords.words(‘english’) to fetch a
list of stopwords in the English dictionary, after
which they are removed. Stop words are words
such as “the”, “a”, “an”, “in”, which are not
significant and do not affect the meaning of the
data to be interpreted.
3) To remove punctuation, we save only the characters that are not punctuation, which can be checked
by using string.punctuation .
4) Stemming: Stemming is a process of linguistic normalization, which reduces words to their
word root word. We stem the tokens using
nltk.stem.porter.PorterStemmer to get the stemmed
tokens. For example, connection, connected, connecting word reduce to a common word ”connect”.
5) Digit removal: We also filtered out any numeric
content as it doesn’t contribute to cyberbullying.
6) Now the next step was to extract features so that
it can be used with ML algorithms, for which
we used TF-IDF Transform using Python’s sklearn
libary. TF-IDF is a statistical measure to evaluate
the relevance of a word, which is basically calculated by multiplying the number of times that
words appeared in the document by the inverse
document frequency of the word. TF-IDF uses the
method diminishing the weight (importance) of
words appeared in many documents in common,
considered them incapable of discerning the documents, rather than simply counting the frequency
of words as CountVectorizer does. The outcomematrix consists of each document (row) and each
word (column) and the importance (weight) computed by tf * idf (values of the matrix). If a word
has high tf-idf in a document, it has most of the
times occurred in given documents and must be
absent in the other documents. So the words must
be a signature word.
# Result :
![image](https://user-images.githubusercontent.com/99632495/236155593-b2749feb-a694-4f19-950f-c79d23f51bfa.png)

## Contact Links : 
-Twitter : https://twitter.com/AbhiShek6903

-Email : abhiabhishek6903@gmail.com

-Linkedin : https://www.linkedin.com/in/abhishek-sharma-5914bb206

Happy Hacking ... Abhishek Sharma :)

