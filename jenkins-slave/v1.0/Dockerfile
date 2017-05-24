FROM cloudbees/jnlp-slave-with-java-build-tools-dockerfile

RUN /bin/bash -c 'sudo yum update -y &&\
                    sudo yum install -y docker &&\
                    sudo service docker start && \
                    sudo usermod -a -G docker jenkins'

ENTRYPOINT ["/opt/bin/entry_point.sh", "/usr/local/bin/jenkins-slave"]