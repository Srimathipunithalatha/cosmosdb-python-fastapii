
# python base image in the container from Docker Hub
FROM python

## copy files to the /app folder in the container
COPY ./requirements.txt /app/requirements.txt

COPY ./main.py /app/main.py


## set the working directory in the container to be /app
WORKDIR /app

## install the packages from the Pipfile in the container
RUN pip install fastapi
RUN pip install fastapi uvicorn
RUN pip install python-dotenv
RUN pip install aiohttp
RUN pip install azure-cosmos
RUN pip install routes

# expose the port that uvicorn will run the app on
ENV PORT=8080
EXPOSE 8080

# execute the command python main.py (in the WORKDIR) to start the app
CMD ["python", "main.py"]