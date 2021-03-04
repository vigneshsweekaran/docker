FROM alpine:latest

RUN apk add curl bash

RUN curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

RUN chmod +x kubectl && \
    mv kubectl /usr/local/bin/
    
CMD ["sleep", "infinity"]
