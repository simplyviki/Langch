

***********
Python-dotenv is a Python module that allows you to specify 
environment variables in traditional UNIX-like “.env” (dot-env) 
file within your Python project directory

Python-dotenv reads key-value pairs from a .env file and can 
set them as environment variables. It helps in the development 
of applications following the 12-factor principles.

load_dotenv()  # take environment variables from .env
reference url: https://pypi.org/project/python-dotenv/#:~:text=Python%2Ddotenv%20reads%20key%2Dvalue,following%20the%2012%2Dfactor%20principles.
By default, load_dotenv doesn't override existing environment variables.
************
https://pypi.org/project/streamlit/

Streamlit lets you turn data scripts into shareable web apps in minutes, not weeks. It’s all Python, open-source, and free! And once you’ve created an app you can use our Community Cloud platform to deploy, manage, and share your app.

command to deploy: streamlit run main.py
*****************
PyPDF2 is a free and open-source pure-python PDF library capable of splitting, merging, cropping, and transforming the pages of PDF files. It can also add custom data, viewing options, and passwords to PDF files. PyPDF2 can retrieve text and metadata from PDFs as well.

***************
langchain.text_splitter
This is the simplest method. This splits based on characters (by default “\n\n”) and measure chunk length by number of characters.

How the text is split: by single character

How the chunk size is measured: by number of characters
*************
from langchain.embeddings.openai import OpenAIEmbeddings
https://python.langchain.com/en/latest/reference/modules/embeddings.html?highlight=OpenAIEmbeddings#langchain.embeddings.OpenAIEmbeddings

Wrapper around OpenAI embedding models.

To use, you should have the openai python package installed, and the environment variable OPENAI_API_KEY set with your API key or pass it as a named parameter to the constructor.

"OpenAI embeddings provide access to datasets with higher dimensionality than open-dense models, allowing them to perform tasks such as clustering and dimensionality reduction. OpenAI embeddings can also be used to create input data for clustering and to answer questions based on the data"

https://platform.openai.com/docs/guides/embeddings

embeddings convert text into vector equivalent numbers
***************
from langchain.vectorstores import **FAISS**

Facebook AI Similarity Search (Faiss) is a library for efficient similarity search and clustering of dense vectors. It contains algorithms that search in sets of vectors of any size, up to ones that possibly do not fit in RAM. It also contains supporting code for evaluation and parameter tuning.

*****************************
from langchain.chains.question_answering import load_qa_chain


from langchain.llms import OpenAI
*****************
from langchain.callbacks import get_openai_callback
https://python.langchain.com/en/latest/modules/models/llms/examples/token_usage_tracking.html

This notebook goes over how to track your token usage for specific calls. It is currently only implemented for the OpenAI API.

Let’s first look at an extremely simple example of tracking token usage for a single LLM call.

**Tokens**: 
https://help.openai.com/en/articles/4936856-what-are-tokens-and-how-to-count-them
Tokens are the basic unit that OpenAI GPT models (including ChatGPT) use to compute the length of a text. They are groups of characters, which sometimes align with words, but not always. In particular, it depends on the number of characters and includes punctuation signs or emojis.

” Prompt tokens are the parts of words fed into GPT-4 while completion tokens are the content generated by GPT-4