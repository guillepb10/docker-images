FROM cloudbees/jnlp-slave-with-java-build-tools

USER root

# set up docker repos
RUN apt-get install apt-transport-https ca-certificates curl software-properties-common
RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -
RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

# install docker
RUN apt-get update
RUN apt-get --yes --force-yes install docker-ce

# give docker access to jenkins
RUN usermod -G docker jenkins