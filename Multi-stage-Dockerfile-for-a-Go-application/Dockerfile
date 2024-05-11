# Build Stage 
FROM golang:1.18-alpine AS builder
WORKDIR /app
COPY . . 
RUN go mod init example/hello && go mod tidy && go build -o hello
#Final Stage 
FROM alpine:latest
WORKDIR /root/
#Copying the compiled app from the prev stage 
COPY --from=builder /app/hello .
EXPOSE 8080 
CMD ["./hello"]

