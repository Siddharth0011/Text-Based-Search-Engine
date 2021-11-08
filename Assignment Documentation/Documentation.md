## jsonconverter.py
    - This file is used to convert our corpus which is "music.json" to individual json file where each individual json file all the information about a single song.

## jsonconverter()
    - Function for creating individual json files for storing each song's details.
    - Data taken from: music.json
    - Data stored in: /json-files

## store_artist_name_list.py
    - This file helps in getting the names of artists and bands from our corpus and saving it as artist_name_list.json

## create_artist_name_list()
    - Function for storing unique artist and band names.
    - Data taken from: /json-files
    - Data stored as: /savers/artist_name_list.json

## category.py
    -  This file helps in getting the names of category or genre from our corpus and saving it as category.json
  
## create_artist_name_list()
    - Function for storing unique categories.
    - Data taken from: /json-files
    - Data stored as: /savers/categories.json

## store_document_tokens_list.py
    - create_document_tokens_list() is being called which is tokenizing the file.

## create_document_tokens_list();
    -  This file helps in storing the tokenized words we get from each document as lists and then the corresponding list is stored         document_tokens_list.json
    - Data taken from: /json-files
    - Data stored in: /savers/document_tokens_list.json

## store_vocabulary.py
    - This files helps in storing all the unique words which are present in our corpus and store it as a json file(vocabulary.json)
    - The functions used are:
    - compute_vocabulary()
    - build_vocabulary()

## compute_vocabulary():
    - Function is retreiving the document_tokens_list to create the vocabulary,then storing the vocabulary in a json file
    - Data taken from : /savers/document_tokens_list.json
    - functions called : build_vocabulary(document_tokens)
    - Data stored in : /savers/vocabulary.json

## build_vocabulary():
    - Function for building the vocabulary i.e. the dictionary which has all the unique words in the corpus
    - Parameters given: document_tokens

## store_megadict.py
    - This files helps in creating a mega dictionary which contains the words in the vocabulary as the key and the value as another dictionary which contains each document as key and its value is one more dictionary as which contains the TF,IDF and TF-IDF values.
    - The structure of dictionary is as follows-
    - It is a nested dictionary which contains-
    - Dictionary1-containing word of vocabulary
        - Dictionary2-containing the document number
            - Dictionary3-contains Tf,Idf,Tf_idf for each document

    - Data for making the above dictionary is taken from
    1.Vocabulary - list of all word in the dictionary.
    2.Document Token list - list of all files containing songs.


## Descriptions of function-

### buildIDF()--
    For counting the number of documents in which a word is appearing.

### buildFreqDist()--
    For counting the frequency of each word in the particular document.

### returnIdf()--
    Returns the calculated idf for each word for each document.

### returnTermFrequency()--
    Returns the tf value of each term in a document.


## document_normalized_denominator.py

    This file help in precalculation of the normalized length of each documents and then store it as a json file(normaliseddenom.json)

## store_scores_gui.py
    Data accessed from :
    - /savers/primeDictionary.json
    - /savers/normaliseddenom.json
    - /savers/score.json

    Functions called:
    - terminal_function()
    - process_function()

    Data returned to :
    - /savers/store.json

### process_function()
    - Function for inputting query and performing query based operations and finally calculating cosine scores. It performs the following features:
    1. Applying stemming porting on query
    2. calculating tf and idf for query
    3. for every word in query_wt we parse all documents

## final_gui.py
    - This file is for creating the GUI as well as processing the query based on song name, artist and band names and categories. It uses Flask framework for the front-end work. CSS and JS files are provided in separate folders.

    - Functions used:
    1) homepage()- This is the homepage
    2) categories() - Displays the different famous song categories
    3) result() - This is used to create GUI of the final results page consisting of 10 results. It uses process_function() of store_scores_gui.py
