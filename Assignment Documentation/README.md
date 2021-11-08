## Order of executing the files.
```
 - jsonconverter.py
 - store_artist_name_list.py
 - category.py
 - store_document_tokens_list.py
 - store_vocabulary.py
 - store_megadict.py
 - document_normalized_denominator.py
 - store_scores_gui.py
 - final_gui.py

``` 

## Group members
1. Rahul Prakash    -- 2018AAPS0893H
2. Siddharth Raj    -- 2018AAPS0398H
3. Ketan Goyal      -- 2018A8PS0900H


<-Screenshots->
1) Offline
	(Path= ./Screenshots/)


## Built and Tested on Machine with following specs:
1) Processor: i5 8250U
2) RAM- 8GB DDR4
3) OS- Windows 10 Home 
## The following files which contain python codes have been used for making this project:

1. jsonconverter.py:
  This file is used to convert our corpus which is "music.json" to individual json file where each individual json file all the information about a single song
  
2. store_artist_name_list.py:
  This file helps in getting the names of artists and bands from our corpus and saving it as artist_name_list.json
  
3. category.py
  This file helps in getting the names of category or genre from our corpus and saving it as category.json
  
4. store_document_tokens_list.py:
  This file helps in storing the tokenized words we get from each document as lists and then the corresponding list is stored document_tokens_list.json

5. store_vocabulary.py:
  This files helps in storing all the unique words which are present in our corpus and store it as a json file(vocabulary.json)

6. store_megadict.py:
  This files helps in creating a mega dictionary which contains the words in the vocabulary as the key and the value as another dictionary which contains each document as key and its value is one more dictionary as which contains the TF,IDF and TF-IDF values.

7. document_normalized_denominator.py:
  This file help in precalculation of the normalized length of each documents and then store it as a json file(normaliseddenom.json)

8.  store_scores_gui.py:
  This file is used to take query as input and then it helps in calculating the scores for each document and store it as a json file(score.json).

9. final_gui.py: 
  This is the file containing the final gui program and is writtem in flask framework for python. Its function is to take query and return or receive the names of the 10 most relevant documents,i.e, top 10 documents with the highest scores which we calculated using TF-IDF method


## Creating the GUI

We have used Flask Framework V-1.0.2 for creating the GUI. It is used for easy creation of front-end of our webpage. This Flask Framework is written in Python.

The user can search for the songs using the full name or part of full name of the song, artist or band name or genre using the search box present in the homepage of our Search Engine. The result displayed will contain the top 10 most relevant songs along with their Artist or Band Names, Album Names, Genres and Duartion.

In the Search Engine there are also options for searching songs based on Popular Artist or Band and Genre as well.






