# Use the official Rust image as the build stage
FROM rust:latest

# Set the working directory
WORKDIR /app

# Copy the source code into the container
COPY . .

# Build the application in release mode
RUN cargo build --release

# Expose the port the server will run on
EXPOSE 1339

# Run the compiled binary
CMD ["./target/release/aluminium"]