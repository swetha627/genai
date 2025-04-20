**Agentic AI** - These system are designed to autonomously reason, plan and execute complex tasks based on high-level goals.
  For example: An AI Agent tasked with buildling a website could autonomously manage tasks like layout desig, writing html and css codes, connectanding backend processes, generating content
              and debugging all while requiring minimal human input.

Components of AI Agents:

**LLM:** Brain of an Agent, responsible for co-ordinating, decision-making. The Agents core is where the agents overall goals and objectives are defined and orchestrated.

**Memory Modules:** - AI Agents rely on memory to maintain context and adapt to ongoing or historical events

  **Short-Term Memory:** Tracks agents ToT and recent actions, ensuring context is preserved throughout the current flow.
  
  **Long_term Memory:** Retains historical interactions and relevant information, allowing for deeper contextual understanding and improved decision-making over time

**Planning Module**:
  
  Enable complex task into actionable steps
  
  **Without Feedback**: allows CoT/ToT to decompose complex tasks into simpler ones
  
  **With Feedback**: Involved ReAct, Reflexion or human in the feedback loop for refined strategies and outcome.

**Tools**:

AI Agents can extend their capabilities by integrating with external tools such as API'S, Database, RAG pipelines and other AI models

User request -----> LLM --------> planning module ------> Memory Module --------> Tool Integration -------> Reasoning and Reflexion

