FROM python:alpine
WORKDIR /myapp
COPY . .
RUN pip install -r requirements.txt
EXPOSE 80
CMD ["python", "app.py"]