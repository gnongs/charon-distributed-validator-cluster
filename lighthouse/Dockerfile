FROM sigp/lighthouse:v3.1.2

RUN apt-get update && apt-get install -y curl jq wget

ENV YQ_VERSION=v4.27.5
ENV YQ_BINARY=yq_linux_amd64
RUN wget https://github.com/mikefarah/yq/releases/download/${YQ_VERSION}/${YQ_BINARY} -O /usr/bin/yq \
    && chmod +x /usr/bin/yq

ENTRYPOINT ["/opt/charon/lighthouse/run.sh"]
