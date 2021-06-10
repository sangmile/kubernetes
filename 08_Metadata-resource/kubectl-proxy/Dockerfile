FROM alpine
RUN apk update && apk add curl && curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl" && install -o root -g root -m 0755 kubectl /bin/kubectl
COPY kubectl-proxy.sh /kubectl-proxy.sh

RUN ["chmod", "+x", "/kubectl-proxy.sh"]
ENTRYPOINT ["/kubectl-proxy.sh"]