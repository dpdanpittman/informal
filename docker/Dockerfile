FROM ubuntu:22.04

# Install dependencies
RUN apt-get update && \
    apt-get install -y openssl libssl-dev pkg-config cargo

# Set the working directory
WORKDIR /app

# Copy the Trust-DNS repository
COPY . .

# Build the Trust-DNS application
RUN cargo build --release --all-features -p trust-dns

# Define the command to run the application
CMD ["./target/release/trust-dns", "-c", "./tests/test-data/test_configs/example.toml", "-z", "./tests/test-data/test_configs/", "-p", "24141"]