# Use the current Long Term Support (LTS) version of Node.js
FROM node:lts

# Copy the matchmaker server source code from the build context
COPY /Matchmaker /Matchmaker

# Install the dependencies for the matchmaker server
RUN Matchmaker/platform_scripts/bash/setup.sh

# Expose TCP ports 90 and 9999
EXPOSE 90
EXPOSE 9999

# Set the matchmaker server as the container's entrypoint
ENTRYPOINT ["/usr/local/bin/node", "/Matchmaker/matchmaker.js"]
