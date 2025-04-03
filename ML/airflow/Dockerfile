FROM apache/airflow:2.6.0-python3.9

USER root
RUN mkdir -p /app/models
RUN echo "DOCKERFILE WAS READ SUCCESSFULLY" > /tmp/buildtest.txt

# Switch to airflow user for Python package installation
USER airflow
COPY requirements.txt /tmp/requirements.txt
RUN pip install --upgrade pip && \
    pip install -r /tmp/requirements.txt 
USER airflow
# Ensure the installation is in Python path
ENV PYTHONPATH=/home/airflow/.local/lib/python3.9/site-packages:${PYTHONPATH}