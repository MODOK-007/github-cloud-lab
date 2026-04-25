FROM mcr.microsoft.com/devcontainers/base:ubuntu

WORKDIR /app

# Instalujemy pythona systemowo, skoro nie możemy pobrać gotowego obrazu
RUN apt-get update && apt-get install -y python3 python3-pip
RUN ln -s /usr/bin/python3 /usr/bin/python

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt --break-system-packages

COPY app.py .

EXPOSE 5000

CMD ["python", "app.py"]
