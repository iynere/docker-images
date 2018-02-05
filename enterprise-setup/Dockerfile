FROM circleci/python:2.7.14-jessie

USER root

# install terraform
RUN wget https://releases.hashicorp.com/terraform/0.9.9/terraform_0.9.9_linux_amd64.zip && \
	unzip terraform_0.9.9_linux_amd64.zip && \
	rm -f terraform_0.9.9_linux_amd64.zip && \
	mv terraform /usr/local/bin

# install aws cli
RUN wget https://s3.amazonaws.com/aws-cli/awscli-bundle.zip && \
	unzip awscli-bundle.zip && \
	rm -f awscli-bundle.zip &&  \
	./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws && \
	rm -r awscli-bundle

USER circleci