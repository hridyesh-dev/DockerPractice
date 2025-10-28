
FROM python:3.7 

WORKDIR /app

COPY . .

#command to install all the dependencies
RUN pip install -r  requirements.txt

#yeh hamesha chalega 
ENTRYPOINT ["python"]

#agar external koi command nahi dala toh run.py chalega 
#but this can also be overridden
CMD [ "run.py" ]
