FROM python:3.10.6
WORKDIR /app/
COPY /dist/ds-service-1.0.tar.gz .
RUN pip install --no-cache-dir ds-service-1.0.tar.gz
RUN pip install --no-cache-dir kafka-python 
# Set the environment variable for the Flask app
ENV FLASK_APP=src/app/__init__.py

# Expose the port
EXPOSE 8010

# Start the Flask app
CMD ["flask", "run", "--host=0.0.0.0", "--port=8010"]
