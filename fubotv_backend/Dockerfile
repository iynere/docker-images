FROM circleci/node:6.11.1

USER root

RUN curl https://sdk.cloud.google.com | bash && \
		~/google-cloud-sdk/bin/gcloud components update kubectl

USER circleci