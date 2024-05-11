FROM python:3.8-slim
ENV PYTHONDONTWRITEBYTECODE=1 
# Prevents Python from writing pyc files to disk
ENV PYTHONUNBUFFERED=1
#Ensures Python output is logged immediately
WORKDIR /code
COPY requirements.txt /code/
RUN pip install --no-cache-dir -r requirements.txt
COPY . /code/
CMD [ "flask","run","--host=0.0.0.0" ]
