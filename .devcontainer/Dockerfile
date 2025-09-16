# Use the official n8n image
ARG N8N_VERSION=latest
FROM n8nio/n8n:${N8N_VERSION}

USER root

# Update & install ffmpeg & python/pip
RUN apk update && \
    apk add --no-cache ffmpeg python3 py3-pip curl

# Install yt-dlp via pip
RUN pip3 install --no-cache-dir yt-dlp

# (Optional) if you want to download latest binary instead of pip, could e.g.:
# RUN curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp && \
#     chmod a+rx /usr/local/bin/yt-dlp

# Return to non-root user
USER node

# You can optionally set environment variables here, or leave to Render UI
# Expose port, etc. The n8n image already sets defaults.

# Default CMD is inherited from base image, so no need to explicitly declare

