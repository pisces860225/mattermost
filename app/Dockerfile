# Using the official Mattermost Team Edition image from Docker Hub with the latest tag
FROM mattermost/mattermost-team-edition:latest

# Some ENV variables
ENV PATH="/mattermost/bin:${PATH}"

# Install necessary packages
RUN apt-get update && apt-get install -y curl jq && rm -rf /var/lib/apt/lists/*

USER mattermost

# Copy any additional scripts or files if needed
# COPY entrypoint.sh /
# ENTRYPOINT ["/entrypoint.sh"]

WORKDIR /mattermost
CMD ["mattermost", "--config", "/tmp/config.json"]
