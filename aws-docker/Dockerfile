FROM ubuntu:18.04


RUN apt-get update && \  
apt-get install -y curl unzip wget

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && unzip awscliv2.zip && \
./aws/install && \
curl -o kubectl https://amazon-eks.s3.us-west-2.amazonaws.com/1.18.9/2020-11-02/bin/darwin/amd64/kubectl \
&& chmod +x ./kubectl && mkdir -p $HOME/bin && cp ./kubectl $HOME/bin/kubectl && export PATH=$PATH:$HOME/bin \
&& echo 'export PATH=$PATH:$HOME/bin' >> ~/.bashrc && \
curl -o aws-iam-authenticator https://amazon-eks.s3.us-west-2.amazonaws.com/1.18.9/2020-11-02/bin/linux/amd64/aws-iam-authenticator && \
chmod +x ./aws-iam-authenticator && \
mkdir -p $HOME/bin && cp ./aws-iam-authenticator $HOME/bin/aws-iam-authenticator && export PATH=$PATH:$HOME/bin && echo 'export PATH=$PATH:$HOME/bin' >> ~/.bashrc

RUN wget https://get.helm.sh/helm-v3.4.2-linux-amd64.tar.gz && \
tar -zxvf helm-v3.4.2-linux-amd64.tar.gz && \
mv linux-amd64/helm /usr/local/bin/helm && rm -rf awscliv2.zip helm-v3.4.2-linux-amd64.tar.gz


