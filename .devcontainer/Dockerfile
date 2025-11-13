# Small Python 3.13 image
FROM python:3.13-slim AS dashboard

# Install OS packages needed for Python + Streamlit
RUN apt-get update && apt-get install -y --no-install-recommends \
    git \
    build-essential \
    curl

# Working directoryW
WORKDIR /workspace

# Install Python dependencies from requirements.txt file
COPY ../requirements.txt /workspace/requirements.txt
RUN pip install --upgrade pip && \
    pip install -r requirements.txt

# The code to run when container is started:
# Common practice to keep the Docker container running without performing any significant action. 
ENTRYPOINT ["tail", "-f", "/dev/null"]