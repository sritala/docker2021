
FROM golang:1.15.0
EXPOSE 8080

## Install golang 

# ENV Port if it's not default
ENV PORT=8080

# Copy content
COPY . /usr/src/app

# Build static files
RUN go build

# Do tests
RUN go test ./...

# Environment variable if not default
ENV PORT=8080
ENV REQUEST_ORIGIN=http://localhost:5000

# Run the application
CMD ["./server"]