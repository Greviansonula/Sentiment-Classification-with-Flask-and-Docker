FROM python:3.8

COPY requirements.txt .

RUN  pip install -r requirements.txt

RUN python -c "import nltk; nltk.download('omw-1.4'); nltk.download('wordnet')"

RUN pip install Flask

RUN which flask

COPY . .

EXPOSE 5000

CMD ["flask", "run", "host=0.0.0.0" "--port=5000"]