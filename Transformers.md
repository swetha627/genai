# **Transformers and Sequence Modeling**

## **Sequence Modeling**  
Building a system that can predict the next token in a sequence is called **Sequence Modeling**. The **Transformers** architecture is highly effective in predicting the next token in a sequence.  

## **Transductive Learning**  
Transductive Learning is a scenario where a model is trained with a **limited amount of labeled text data** alongside a **larger set of unlabeled data**.  

---

## **Recurrent Models**  
Recurrent models generate the next token based on the previous token in a **sequential manner**.  
- This approach works well for **short sequences** but struggles with **longer sequences** due to memory limitations and vanishing gradients.  

---

## **Attention Mechanism**  
The **attention mechanism** calculates weights to determine how much focus should be placed on different parts of the input data.  
- This allows the model to prioritize information from the most relevant parts of the input.  
- **Recurrent Neural Networks (RNNs)** struggle to retain information from earlier parts of a sentence.  
- To solve this, researchers combined **RNNs + Attention**, but memory issues persisted.  
- The solution was to **remove RNNs completely** and introduce **Transformers**.  
- This concept was introduced in the paper **"Attention Is All You Need"**.  

---

## **Self-Attention**  
- Self-Attention allows the model to look at all parts of the input sentence and determine the importance of each word in relation to every other word.  

---

## **Encoder-Decoder Architecture in Transformers**  

### **Encoder**  
The encoder converts the input into a specific format called **embeddings**.  

#### **Step 1: Multi-Head Self-Attention**  
- The attention process is **split into multiple heads**, where each head performs its own attention computation in parallel.  
- Each computation is different, and the outputs are then combined to form the final output.  

#### **Step 2: Fully Connected Feed-Forward Network**  
- This takes the **normalized input** from the encoder and applies additional transformations to enhance the model's understanding of the input.  

---

### **Decoder**  
The decoder **uses embeddings from the encoder's output** to predict the next token in an **auto-regressive manner** (each generated token is used as input for the next step).  

#### **Example of Auto-Regressive Generation:**  
- **Step 1:**  
  - **Input:** `gen ai is`  
  - **Output:** `gen ai is interesting`  
- **Step 2:**  
  - **Input:** `gen ai is interesting`  
  - **Output:** `gen ai is an interesting domain`  

#### **Decoder Components:**  
1. **Masked Multi-Head Attention Layer:**  
   - The model **must not look at future tokens** while predicting the next token.  
2. **Cross-Attention Layer:**  
   - This sublayer **uses encoder embeddings** to understand the context and generate the next appropriate token.  
3. **Fully Connected Feed-Forward Network:**  
   - Helps refine the decoder's understanding of the input and its context.
