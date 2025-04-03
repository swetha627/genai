Transformers is an effective architecture to predict the next token in the sequence.

Building a system that can predict the next token in the sequence is called Sequence Modelling.

Transductive Learning: It the scenerio where a model is trained with limited amount of labled text data alongside a larger set of unlabeled data.

Recurrent Models: These generate next token based on the previous token sequentially. This approcah is good for short sequences but not for longer sequence.

Attention: Attention mechanism calculates weights,  determining how much focus in on the input data part. The process enable the model to prioritize info from the parts of
           input more relevant to the task.

            Models like RNN struggle to give importance for the information from the early parts of the sentence.
            But Attention allows to "look back" at all input parts of the sentence
            So they combined RNN + Attention, but still there were memory issues. So they removed RNN and introduced transformers "ATTENTION IS ALL YOU NEED"

Self- Attention: We look at all the parts of the sentence and understand how important each part is when compared to every other part


Encoder and Decoder:

Encoder: Converts input into specific format called Embeddings.

step 1: 
  
  Multi-head self-attention:
    Splitting attention process into "multiple heads" where each head performs its own attention computation parallely. Each computation will be different. Each head produces
        output which is then combined together to get the final output
step 2:
  
  Fully connected feed-forward network:
    This takes in the normalised input from the encoder and performs more transformations to help model understand inputs better

      


Decoder: Use Embeddings from the output of encoders to predict the next token in the sentence. It is called "Auto Regressive" manner. 
         token generated from the input is again combined with input for the next step
        
         step 1:
        
          Input - gen ai is
          Output - gen ai is intresting
        
         step 2:
        
          Input - gen ai is intresting
          Output - gen ai is intresting domain

  step 1: Masked Multi-head Attention layer - prediction of the next token should soley depend on the previous token so avoid looking on to the future tokens
          Cross attention layer - Sublayer that uses encoders embeddings to understand the context and generate the next appropriate token
          Fully connected feed forward - to refine the decoders understanding input and its context.


        





