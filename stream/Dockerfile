FROM python:3.8

# Install CMake for gqlalchemy
RUN apt-get update && \
  apt-get --yes install cmake && \
  rm -rf /var/lib/apt/lists/*

# Install packages
COPY requirements.txt ./
RUN pip3 install -r requirements.txt

COPY stream.py /app/stream.py
COPY friendship_network_stream.csv /app/friendship_network_stream.csv

WORKDIR /app
