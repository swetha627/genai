Pre-Training:
  
  Before fine-tuning a model for specfic usecase, we train model with large amount of unlabelled text data helping model to 
  
    1. Absorb general linguistic knowledge from the large corpora
  
    2. Develop a depp understanding of syntax, semantics and facts
  
    3. Required little labelled data for fine-tuning
  
  Pre-Training uses self-supervised learning to train models with unlabeled data

What is **Self-Supervised Learning**:

  Models learns from unlabled data by generating its own labels


Types of Pre-training:

1. **Casual Language Modelling:**
  
  Model predicts the next word given previous words. This is an auto-regressive structure

2. **Masked Language Modelling:**

  Model predicts missing words in the sentence. Allows models to learn from left and right, and right to left - both the contexts.

3. **Encoder-Decoder Pre-Training:**

  Encoder process an inout sentence and Decoder generates a corresponding output sentence


 
