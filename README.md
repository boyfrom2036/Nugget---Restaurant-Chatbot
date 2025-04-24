# Nugget---Restaurant-Chatbot

Project Summary
This project implements a Retrieval-Augmented Generation (RAG) chatbot focused on answering user queries about restaurants in Roorkee, as part of the Zomato Gen AI Internship Assignment. The system is built through several key steps:

Web Scraping:
Using Selenium, BeautifulSoup, and Pandas, I scraped menus and metadata (name, price, type, ratings, hours, etc.) for 7 Roorkee restaurants from Zomato. Care was taken to respect ethical scraping practices, including delays and robots.txt compliance.

Data Preprocessing & Feature Engineering:
I cleaned and enriched the dataset by filling missing descriptions, classifying dishes by price range (cheap, moderate, expensive), and creating composite tags for better searchability. The final dataset contains 1375 menu items with new features like "dish type" and "tag".

Data Transformation:
The processed CSV data was converted into structured JSON documents, combining human-readable summaries with machine-friendly metadata, ready for semantic retrieval.

RAG Pipeline:
Menu and restaurant data were embedded using the sentence-transformers/all-mpnet-base-v2 model and stored in Pinecone for fast similarity search. The chatbot uses MistralAI to generate responses strictly based on retrieved context, with prompt engineering to ensure domain focus and refusal of out-of-scope queries.

User Interface:
A Streamlit web app provides a real-time chat interface, displaying answers, chat history, and contextual information in an accessible format.

Results:
The chatbot can answer a wide range of queries, such as price ranges, best vegetarian options, dessert prices, spice level comparisons, and budget-friendly recommendations, using only the data scraped from Zomato.

Challenges & Solutions:
I addressed dynamic content scraping with Selenium, controlled language model output with strict prompts, and overcame latency issues by switching from local Hugging Face models to MistralAI for faster response times.

Future Improvements:
Planned enhancements include adding conversational memory, real-time data updates, and multimodal (image+text) search capabilities.

Conclusion:
This project gave me hands-on experience with real-world data pipelines, semantic search, and conversational AI. It improved my technical skills and showed how AI can provide practical solutions in the food-tech domain, despite challenges like dynamic web content and model latency.

How to run this file:
1. download all the files
2. create the environment
3. scrape the data and convert it into all single csv file
4. preprocess and create a new feature of your own
5. data_converter to convert the data into json file
6. ingest to send the json data to the pinecone vectordatabase
7. rag_pipeline to buld the RAG
8. app2.py for the streamlit ui


Rest Clear instruction have been given in the video on how 
to run the chatbot in the local machine
