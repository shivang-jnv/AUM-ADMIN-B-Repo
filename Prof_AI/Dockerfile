FROM python:3.10-slim

RUN apt-get update && apt-get install -y procps && rm -rf /var/lib/apt/lists/*

WORKDIR /app

COPY requirements.txt .

# Install requirements directly to the container
RUN pip install -r requirements.txt

COPY . .

EXPOSE 8000

RUN chmod +x start_voice_agent.sh

CMD ["./start_voice_agent.sh"]
