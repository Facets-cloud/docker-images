FROM ubuntu:latest
RUN apt-get update && apt-get install curl jq unzip python3 -y
RUN update-alternatives --install /usr/bin/python python /usr/bin/python3 10
RUN curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"
RUN unzip awscli-bundle.zip
RUN ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws
RUN curl -LO https://dl.k8s.io/release/v1.21.0/bin/linux/amd64/kubectl
RUN install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
