# syntax=docker/dockerfile:1

FROM golang:1.19-alpine3.16

# Set destination for COPY
RUN mkdir /app
WORKDIR /app

# Download Go modules
COPY go.mod ./
COPY go.sum ./
RUN go mod download

# Copy the source code. Note the slash at the end,
# means we are copying to the current workdir which is /app
COPY *.go ./

# Build executable file inside /app dir
RUN go build -o main .

# To actually open the port, runtime parameters
# must be supplied to the docker command.
EXPOSE 8080

# Run
CMD ["./main"]