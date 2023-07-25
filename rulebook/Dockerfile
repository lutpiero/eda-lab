# Base image
FROM ubuntu:latest

# Install Java JDK 1.8
RUN apt-get update && \
    apt-get install -y openjdk-17-jdk

# Install Python 3 and pip
RUN apt-get install -y python3 python3-pip
RUN apt-get install -y curl

# Install Ansible
RUN pip3 install "ansible<2.11"
RUN pip3 install jinja2==3.0.3 --force-reinstall
RUN pip3 install Flask --upgrade
RUN pip3 install pyyaml==5.3.1
RUN pip3 install packaging==21.0
RUN pip3 install resolvelib==0.8.1

RUN python3 -m pip show jinja2

# Set environment variables
ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
ENV PATH=$PATH:$JAVA_HOME/bin

# Install Ansible Rulebook & galaxy
RUN ansible-galaxy collection install ansible.posix
RUN ansible-galaxy collection install community.general
RUN ansible-galaxy collection install ansible.eda
RUN pip3 install ansible ansible-rulebook ansible-runner

# Set working directory
WORKDIR /app

# Copy your application files to the container
# COPY . .

# Run your application
#CMD [ "python3", "app.py" ]
