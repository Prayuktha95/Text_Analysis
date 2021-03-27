# Text_Analysis
Analyzing YouTube comments for their sentiments.
For datasets, follow the link below
https://drive.google.com/drive/u/0/folders/10pR3ScH9qT5iq3hvVvE37seRpsaPbIGF

Steps:
I am working with Jupyter notebook. 
Open a new file.
Import the required libraries, they are pandas, numpy, matplotlib, seaborn and textblob. Remeber to install textblob if it is not installed before.
Read the file 'GBcomments.csv' and assign it to 'comments'. Set error_bad_lines to False, this will drop bad lines like lines with too many commas.
Since we are analyzing comments, it is useless to have rows wothout comments. So we drop them.
Create a for-loop to find the polarity of all the comments in the column comment_text. sentiment.ploarity gives the polarity of a text. Try it with a single sentence to help understand how it works.
Create a new column for polarity in the dataframe.
The comments with positive sentiment have a value closer to 1 and the ones with negative polarity have a value closer to -1.
Import wordcloud library. It is used in visual representation of the words and the size of the word depends on its importance. We are using the default list, that is STOPWORDS. This ignores the words like is, was, the, etc and they are not shown in the wordcloud, no matter how high their frequency is.\
To create a wordcloud, join all the comments using .join.
With total_comments, create a wordcloud and plot it. imshow() function is used to display the data in the form of a 2D-image. You can see that the most important words with positive polarity are awesome, best, perfect, love, video, great, look, beautiful. Remember the size of the word indicates its importance.
Repeat the procedure for negative polaity as well and you see that the most frequent and important words are boring, terrible, worst, horrible, etc.
Notice that the word 'video' is present in both positive and negative polarites. It is possible to append your custom stopwords to the default list of stopwords. If you add 'video' to the list of stopwords, then it will be ignored like the rest of the words. 
