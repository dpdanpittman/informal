FROM ubuntu:22.04

# Install dependencies
RUN apt-get update && \
    apt-get install -y openssl libssl-dev pkg-config cargo

# Set the working directory
WORKDIR /app

# Copy the Trust-DNS repository
COPY . /app

# Build the Trust-DNS application
RUN cargo build --release --all-features -p trust-dns

# Define the command to run the application
CMD ["cargo", "run", "--release", "--all-features", "-p", "trust-dns"]