# Base image
FROM ghcr.io/viyancs/eda-rulebook:latest
RUN mkdir /.ansible
RUN chmod -R 777 /.ansible
WORKDIR /app
COPY . .
# extend Install Ansible Rulebook & galaxy
RUN ansible-galaxy collection install ansible.posix
RUN ansible-galaxy collection install community.general
RUN ansible-galaxy collection install ansible.eda
RUN pip3 install ansible ansible-rulebook ansible-runner
RUN ls -lah
EXPOSE 5000

# Run your application
#CMD [ "ansible-rulebook", "-i", "inventory.yml", "--rulebook", "webhook.yml", "-v" ]
