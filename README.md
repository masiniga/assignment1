### 0. Requirements

I used Python version 3.10.4 to run my code.
My code requires the same modules as the base 
code. So, I believe the following would be
more than sufficient.
(These were taken from the class github page.)
```bash
$ pip install spacy
$ python -m spacy download en_core_web_sm
$ pip install flask flask-restful flask-sqlalchemy
$ pip install streamlit graphviz
$ pip install mypy
```


### 1. FastAPI


To run:

```bash
$ uvicorn app_fastapi:app --reload
```

Accessing the API:

There are three URLs. 
The first displays a short description, 
the second displays the named entities,
and the third displays the dependencies.
(They only take a filetype of .json.) 
These are given below. 

```bash
$ curl http://127.0.0.1:8000
$ curl http://127.0.0.1:8000/ner -H "Content-Type: application/json" -d@input.json
$ curl http://127.0.0.1:8000/dep -H "Content-Type: application/json" -d@input.json
```

The URLs below do the same thing but take a
pretty parameter, and display the information
in a nicer format. 

```bash
$ curl http://127.0.0.1:8000?pretty=true
$ curl http://127.0.0.1:8000/ner?pretty=true -H "Content-Type: application/json" -d@input.json
$ curl http://127.0.0.1:8000/dep?pretty=true -H "Content-Type: application/json" -d@input.json
```



### 2. Flask
 
For the flask app, run the command below.

```bash
$ python app_flask.py
```
The website can be accessed at http://127.0.0.1:5000.


### 3. Streamlit

For the streamlit app, run the command below. 

```bash
$ streamlit run app_streamlit.py
```

This can be accessed at  http://localhost:8501/.
