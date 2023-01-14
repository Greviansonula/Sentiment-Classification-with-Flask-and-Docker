
# syntax=docker/dockerfile:1
FROM python:3.8-slim-buster

WORKDIR /api

COPY requirements.txt requirements.txt

RUN  pip3 install -r requirements.txt

RUN python -c "import nltk; nltk.download('omw-1.4'); nltk.download('wordnet')"

COPY . .

EXPOSE 5000

CMD ["python3", "flask", "run", "host=0.0.0.0" "--port=5000"]