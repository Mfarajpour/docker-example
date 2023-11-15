FROM python:alpine

RUN mkdir app

WORKDIR /app
RUN pip install --upgrade pip

RUN pip install gunicorn

COPY ./requirements.txt .

RUN pip install -r requirements.txt

COPY ./app/app.py ./app.py


ENTRYPOINT ["gunicorn"]
CMD ["-b" ,"0.0.0.0:5000","app:app"] 


