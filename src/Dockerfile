### 1. Get Linux
FROM python:3.6


ARG BUILDTIME
ARG REVISION
ARG VERSION=1018.0.308

LABEL org.opencontainers.image.title="thin-edge.io"
LABEL org.opencontainers.image.created=$BUILDTIME
LABEL org.opencontainers.image.version=$VERSION
LABEL org.opencontainers.image.revision=$REVISION
LABEL org.opencontainers.image.description="OPC-UA Demo Server"
LABEL org.opencontainers.image.source="https://github.com/thin-edge/opcua-device-gateway-container"
LABEL org.opencontainers.image.authors="thin-edge.io"
LABEL org.opencontainers.image.vendor="thin-edge.io"
LABEL org.opencontainers.image.licenses="Apache 2.0"
LABEL org.opencontainers.image.url="https://thin-edge.io"
LABEL org.opencontainers.image.documentation="https://thin-edge.github.io/thin-edge.io/"

### 2. Install opcua
RUN pip install opcua
ENV TZ="Europe/Berlin"
### 3. Start server
EXPOSE 4840    
ADD server_generel.py /
CMD ["python3", "server_generel.py"]