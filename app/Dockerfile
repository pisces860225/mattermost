# Using the official Mattermost Team Edition image from Docker Hub
FROM mattermost/mattermost-team-edition:latest

# Set working directory to Mattermost
WORKDIR /mattermost

# Install necessary packages for curl and jq using Alpine's package manager
RUN apk --no-cache add curl jq

# Ensure your entry script is copied and made executable
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh

# Use the entry script as the container's default
ENTRYPOINT ["/entrypoint.sh"]

# Mattermost default command
CMD ["mattermost", "--config", "/tmp/config.json"]
