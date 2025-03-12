**Tokenization** - it is the process of breaking a sentence into words. These words are called Tokens.
    tokens can be words, characters, or subwords.
    Tokenization is classified into 
    1. Sentence Tokenization - sent_tokenize()
    2. Word Tokenization - word_tekenize()
    3. SubWord Toeknization( n gram ) - ngrams()
          example - sentence = Our Team name is Team Data Dynamos
                    N-gram tokens = [('Our','Team','name'),('Team','name','is'),('name','is','Team'),('is','Team','Data'),('Team','Data','Dynamos')]
**Stop Words**: 
    stopwords_en=stopwords.words("english") - to get all the stop words from english lang

**Stemming**:
    1. Porter Stemmer
    2. SnowBall Stemmer
    3. Lancaster Stemmer
    4. Regexp Stemmer


 **Lemmatization**:
    1. Wordnet Lemmatizer
    2. TextBlob Lemmatizer

 **POS Tagging**:

    Adding a parts of speech tag to every word in the corpus. Do not REMOVE Stop Words.
    pos tagging can be done using NLTK and Spacy

  **NER Tagging**:
      Named Entity Recognition is a NLP method that extracts info from text. 
      It detects and categorizes information in the text as named entities 
      NER can be done using NLTK and Spacy
    

 
    
