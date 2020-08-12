# Sarcasm_Detection
### Context
Past studies in Sarcasm Detection mostly make use of Twitter datasets collected using hashtag based supervision but such datasets are noisy in terms of labels and language. Furthermore, many tweets are replies to other tweets and detecting sarcasm in these requires the availability of contextual tweets.
### Dataset 
!wget --no-check-certificate \https://storage.googleapis.com/laurencemoroney-blog.appspot.com/sarcasm.json \-O /tmp/sarcasm.json 
##### Details:
To overcome the limitations related to noise in Twitter datasets, this News Headlines dataset for Sarcasm Detection is collected from two news website. TheOnion aims at producing sarcastic versions of current events and we collected all the headlines from News in Brief and News in Photos categories (which are sarcastic). We collect real (and non-sarcastic) news headlines from HuffPost.
##### Content:
Each record consists of three attributes:
1. is_sarcastic: 1 if the record is sarcastic otherwise 0

2. headline: the headline of the news article

3. article_link: link to the original news article. Useful in collecting supplementary data
### Models and Results:
```1. Simple Embedding Layer```
1. Without considering stop words.
The model achieved vlidation accuracy of ~82.2% and validation_loss of 0.43 .

2. With considering stop words.
The model achieved vlidation accuracy of ~86% and validation_loss of 0.35 .

```2. Along with Conv1D Layer```
(Considering stop words) The model achieved vlidation accuracy of ~83.7% and validation_loss of 0.67 .

```3. Along with Bidirectional Layer```
(Considering stop words) The model achieved vlidation accuracy of ~85% and validation_loss of 0.54 .

