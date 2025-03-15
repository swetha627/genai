**Gen AI**

**Terms**:

Document: each row in dataset is called a document

Corpus: collection of documents is called a corpus

Vocabulary: unique words in corpus

Segmentation: breaking multiple sentences into single individual sentences

Tokenization: breaking sentence into words. each word is called a token

Stop words: common words used in language with less significance

Stemming: process of removing/replacing the suffix of the word to get base word(sometimes meaning of the word can be lost)

Lemmatization: same as Stemming, But here words have dictionary meaning

NER tagging: Named entity recognition

POS tagging: adding parts of speech to each word

Chunking: extracting meaningful phrases/chunks from the sentences


**Preprocessing Techniques**:

Text processing is cleaning text data for analysis and predictions
  1. removal of punctuations, HTMLtags, URL's, extra spaces, **contraction(don't -> do not)**, special characters and numbers

      use re.sub(pattern, replacement, string)
      example to remove {} re.sub(r[\{\}], "", sentence)
  
  3. convert to lowercase - lower() method 
  4. Apply Tokenization
  5. Stop Word removal
  6. Apply Stemming
  7. Apply Lemmatization
  8. POS tagging
  9. Named Enitity Recognition
 
 




