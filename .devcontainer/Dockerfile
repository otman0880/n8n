# Use official prebuilt n8n image (no source build required)
ARG N8N_VERSION=latest
FROM n8nio/n8n:${N8N_VERSION}

USER root

# Install ffmpeg + python + pip
RUN apk update && \
    apk add --no-cache ffmpeg python3 py3-pip curl && \
    pip3 install --no-cache-dir yt-dlp

USER node

