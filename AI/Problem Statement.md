TLDR:

Create an AI-powered chat application with a TypeScript-based Express client that interfaces with a vector database for message retrieval, and a server running a local language model for generating responses. The client should handle incoming chat messages by checking for similar past interactions in the database before querying the server, which will process and return a unique AI-generated response if needed. The response is then stored in the vector database for future reference. Your solution should include proper security measures, handle CORS, and showcase the ability to run an LLM locally. This task assesses your skills for a high-tech generative AI role.

  

---

  

**Technical Coding Challenge:**

  

You are tasked with developing a sophisticated AI chat application utilizing a client-server model, which includes a vector database for retrieving past interactions to ensure consistent responses. This will require knowledge of Express with TypeScript for the client service and the ability to run a Lightweight Language Model (LLM) locally for the server service.

  

**Client Service (Express with TypeScript):**

- Set up an Express server using TypeScript.

- Integrate a vector database (such as Milvus, Weaviate, or Pinecone) to enable efficient message similarity searches.

- Implement an API endpoint `/send-message` that accepts POST requests with JSON payloads structured as `{ message: string }`.

- Before processing a new message, query the vector database for similar messages. If a highly similar message exists, return the associated response.

- If there is no similar message, forward the payload to the server service for AI processing.

- Store the new message and its AI-generated response in the vector database to facilitate future retrieval.

  

**Server Service (Local LLM):**

- Create a server application capable of processing messages with a local LLM, like OpenAI's GPT or a similar model.

- Deploy a RESTful API endpoint `/process-message` that processes POST requests coming from the client service.

- The server should generate a full, immediate AI response for each message without streaming.

- Respond with the AI-generated message in a JSON object `{ reply: string }`.

  

**Interaction Flow and Data Processing:**

- From a browser or Postman, users can send messages to the `/send-message` endpoint of the client service.

- The client service vectorizes the message and checks the vector database for similarity with past queries.

- If a similar query is detected, the corresponding stored response is returned to the user.

- If not, the message is sent to the server service, which uses a local LLM to generate a response.

- This new query-response pair is then stored in the vector database for future reference.

- The client service finally returns the AI's response to the user.

  

**Technical Requirements:**

- Implement message sanitization to protect against injection attacks.

- Properly configure CORS to allow resource sharing as needed.

- Optimize vector database indexing and search thresholds for accurate and efficient matching.

  

**Running LLM Locally:**

- You should be able to demonstrate running an LLM locally, utilizing Python and PyTorch libraries, interfacing with the local server service.

  

**Why This Challenge:**

This challenge aims to assess your technical capabilities for a high-profile generative AI role in India. Your solution will demonstrate your ability to work with advanced AI models, back-end development, and innovative database solutions.

  

Please structure your code and design with the highest standards in mind, as this role requires cutting-edge expertise in the field of generative AI.

  

---

  

For evaluation purposes, please provide the following along with your solution:

- A brief explanation of your design choices, especially for vector database integration and local LLM setup.

- Any assumptions you've made in your implementation.

- Documentation on how to set up and run your services, including any necessary environment setup.

- Unit tests to validate the functionality of both services.