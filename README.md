# Text Mining System

***

## instructions

* Integrated ** text filtering, to weight ** and ** mail real-time notification ** function
* Integrated ** text keyword extraction ** function
* Integrated ** text classification ** ** ** tag function
* Integrated ** text recommended ** ** hot evaluation ** function
* ** English and Chinese support **

## System architecture diagram
![image](Architecture-of-Text-Mining-System.png)

## on the participle
** English participle, the use of nltk toolkit for segmentation **

	pip install nltk 

** Chinese word segmentation, using jieba toolkit for segmentation **

	pip install jieba 

** jieba participle **

	dict main dictionary file
	user_dict user dictionary file, the white list of participles

** user_dict is a white list of participles **
* If the added filter words (including blacklist and whitelist) can not be correctly spelled by jieba correctly, add the word and word frequency to be added into the dict file or the user dictionary user_dict (word frequency can be omitted)

## About stop words, black list, white list

** stopwords is the stop word **
* You can add disabled words at any time, one by one

** blackwords for filtering words blacklist **
* You can add filtered words at any time, one by one

** writewords as keyword whitelist **
* You can add key words at any time, one by one

## About feature words

* Feature words are used for classification to calculate textual features
* The selection of feature words can be determined by the word frequency in the training set
* Feature word dimensions can be set

## About configuration

** config file: **
* Server configuration can be made for the development of the collection of different fields in the database column
* You can limit the number of operating database entries, the default time pushed forward from the recent
* Can choose language (Chinese, English)
* You can set the classification feature dictionary word dimension
* You can set whether to receive mail notification
* You can set the version acceleration, if accelerated classification, the text feature words and classification model will be fixed! Therefore, if you want to test the dimensions of the classification feature dictionary, the features of the classifier and the algorithm, you need to cancel the acceleration.

**program files:**  
* You can change the generation of a feature dictionary, the frequency of words that pass through the word, or the frequency of documents that contain the word
* You can change the text filtering and deduplication algorithm
* You can change the keyword extraction algorithm, optionally based on feature extraction, based on Tf extraction, based on IDf extraction, based on TfIDf extraction, you can change the first K keywords screening method
* You can change the feature generation of the training set and the test set based on feature words, optional Bool features, Tf features, IDf features (no differentiation), TfIDf features, and optionally feature selection or dimensionality reduction
* You can change the text classification algorithm, optional SVC, LinearSVC, MultinomialNB, LogisticRegression, KNeighborsClassifier, DecisionTreeClassifier, you can change the method of algorithm tuning optimization
* You can change the text recommendation algorithm

## other instructions
* Change the word segmentation file dict user_dict lag
Need to manually delete the datas folder beforehand

* Change training set
You need to manually delete all_words_dict and train_datas manually beforehand

* Change the file stopwords blackwords writewords fea_dict_size
Re-run the program can be

## on the environment to build

** Installation of numpy scipy matplotlib under Ubuntu **

    sudo apt-get update
    sudo apt-get install git g++ gfortran
    sudo apt-get install python-dev python-setuptools python-pip
	
    sudo apt-get install libblas-dev liblapack-dev libatlas-base-dev
    export BLAS=/usr/lib/libblas/libblas.so 
    export LAPACK=/usr/lib/lapack/liblapack.so 
    export ATLAS=/usr/lib/atlas-base/libatlas.so
	
	sudo apt-get install python-numpy
	sudo apt-get install python-scipy
	sudo apt-get install python-matplotlib
	or
	sudo pip numpy
	sudo pip scipy
	sudo pip matplotlib	
    
    sudo pip jieba
    sudo pip scikit-learn
    sudo pip simplejson
    sudo pip pymongo

