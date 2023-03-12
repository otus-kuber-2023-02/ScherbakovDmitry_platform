FROM ubuntu:20.04

RUN apt-get update && apt-get install -y python3 python3-pip

COPY . /app

WORKDIR /app

RUN useradd -u 1001 webuser
RUN chown -R webuser:webuser /app
USER webuser

CMD ["python3", "-m", "http.server", "8000"]