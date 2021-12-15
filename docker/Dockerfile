FROM golang:alpine

# Move to working directory /build
WORKDIR /build

# Copy and download dependency using go mod
COPY go.mod .
COPY go.sum .
RUN go mod download

# Copy the code into the container
COPY . .

# Build the application
RUN go build -o main .

# Move to /dist directory as the place for resulting binary folder
WORKDIR /dist

# Copy binary from build to main folder
RUN cp /build/main .

# Env setting datadog site, app key and api key
ENV DD_SITE="datadoghq.??" \
    DD_API_KEY="xxx" \
    DD_APP_KEY="xxx"

# Command to run when starting the container
CMD ["/dist/main"]
