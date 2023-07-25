# Base image
FROM ghcr.io/viyancs/eda-rulebook:latest
WORKDIR /app
COPY . .
RUN ansible-galaxy collection install ansible.eda
RUN ls -lah
EXPOSE 5000

# Run your application
CMD [ "ansible-rulebook", "-i", "inventory.yml", "--rulebook", "webhook.yml", "-v" ]
