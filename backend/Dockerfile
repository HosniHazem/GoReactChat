FROM golang:1.22-alpine

# Install git, bash, gcc, and musl-dev (C standard library)
RUN apk add --no-cache git bash gcc musl-dev

RUN mkdir /app
ADD . /app/
WORKDIR /app

# Download Go modules
RUN go mod download

# Build the Go application
RUN go build -o main .

# Specify the command to run the app
CMD ["/app/main"]
