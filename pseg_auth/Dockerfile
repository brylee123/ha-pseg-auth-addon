FROM alpine:3.20

# Install chromium, chromedriver, ffmpeg, flac, python3, and dependencies
RUN apk add --no-cache \
    python3 \
    py3-pip \
    chromium \
    chromium-chromedriver \
    ffmpeg \
    flac

WORKDIR /app

COPY requirements.txt .
RUN pip install --no-cache-dir --break-system-packages -r requirements.txt

COPY auth_server.py .
COPY run.sh .
RUN chmod +x run.sh

EXPOSE 8000

CMD ["/app/run.sh"]
