# Use the official Ollama image as the base
FROM ollama/ollama:latest

# Install curl
RUN apt-get update && apt-get install -y curl && rm -rf /var/lib/apt/lists/*

# Copy startup script
COPY entrypoint.sh /entrypoint.sh
RUN chmod +x /entrypoint.sh
RUN ls -l /entrypoint.sh  # Debugging step to check if file exists

# Set the entrypoint script
ENTRYPOINT ["bash", "/entrypoint.sh"]