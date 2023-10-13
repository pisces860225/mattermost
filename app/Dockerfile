# Using the official Mattermost Team Edition image from Docker Hub with the latest tag
FROM mattermost/mattermost-team-edition:latest

# Some ENV variables
ENV PATH="/mattermost/bin:${PATH}"

# Install necessary packages using apk
RUN apk add --no-cache curl jq

USER mattermost

# Copy any additional scripts or files if needed
# COPY entrypoint.sh /
# ENTRYPOINT ["/entrypoint.sh"]

WORKDIR /mattermost
CMD ["mattermost", "--config", "/tmp/config.json"]
