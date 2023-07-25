# Base image
FROM viyancs/ansible-rulebook:latest
WORKDIR /app
COPY . .
RUN ls -lah
EXPOSE 5000

# Run your application
CMD [ "ansible-rulebook", "-i", "inventory.yml", "--rulebook", "webhook.yml", "-v" ]
