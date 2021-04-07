FROM kubistmi/pyspark:latest

# Install kubectl
USER root
RUN apt-get update \
  && apt-get install -y apt-transport-https gnupg curl \
  && curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key add - \
  && echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | tee -a /etc/apt/sources.list.d/kubernetes.list \
  && apt update \
  && apt install -y kubectl

# Switch back to Spark USER uid
USER ${UID}