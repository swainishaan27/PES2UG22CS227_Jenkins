FROM jenkins/jenkins:lts

# Switch to root user
USER root

# Update and install required packages in one RUN command
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
    make g++ && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

# Switch back to the Jenkins user
USER jenkins
