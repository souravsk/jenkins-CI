# Use the official Golang image as base image
FROM golang:latest

# Set the working directory inside the container
WORKDIR /app

# Copy the local package files to the container's workspace
COPY . .

# Download and install any required third-party dependencies into the container
RUN go get -d -v ./...

# Build the Go application
RUN go build -o main .

# Expose the port on which the application will run
EXPOSE 9090

# Command to run the executable
CMD ["./main"]
