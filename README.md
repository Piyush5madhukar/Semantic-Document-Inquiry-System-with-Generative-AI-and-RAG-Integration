#Streamlit web application for interacting with PDF documents through a chat interface

![roadmap](https://github.com/Piyush5madhukar/Semantic-Document-Inquiry-System-with-Generative-AI-and-RAG-Integration/assets/105438331/412182a4-9518-4c22-b542-4d31afd9899e)


#LangChain and Dependencies: Importing components from LangChain:
-RecursiveCharacterTextSplitter: For splitting text into chunks.
-GoogleGenerativeAIEmbeddings: For generating embeddings using Google Generative AI.
-FAISS: For building vector stores from text chunks.
-ChatGoogleGenerativeAI and load_qa_chain: For setting up a question-answering chain.
-PromptTemplate: Template for prompting user input.

 
#Steps involved
1)extract text from uploaded PDF documents from PYPDF2
2)split extracted text into manageable chunks
3)generates embeddings for each chunk of text
4)builds a vector store using FAISS (Facebook AI Similarity Search)
5)set up a conversational chain for question-answering
-prompt template
6)Load a local FAISS index  and retrieve relevant documents based on the user's question.
 -Perform similarity search.
7)Set up the Streamlit application
  -Display title
  -text input
  -upload multiple files
 


It leverages Streamlit and LangChain libraries to create an interactive web application for querying information from PDF documents. It integrates PDF text extraction, chunking, embeddings generation, and conversational question-answering capabilities using Google Generative AI and FAISS. The main function orchestrates these components within a user-friendly interface, enhancing accessibility to PDF-based information through a chat-like interaction.

#RAG Integration
1)Retrieval:
-The similarity_search method is used to find relevant documents  based on the user's query.
-The retrieved documents are then combined into a single context.

2)Augmented Generation:
-The get_conversational_chain function creates a prompt template for generating detailed answers from the provided context.
-The chain is used to generate a response using the combined context and the user's question.
-user_input function:
Added context creation by combining retrieved documents.
Passed context and user_question to the conversational chain to generate detailed responses.
By integrating RAG, the system retrieves relevant documents based on the user's query and then generates a detailed response using the context from those documents, providing more accurate and contextually relevant answers.
