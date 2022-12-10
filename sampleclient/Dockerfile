FROM golang:1.16-alpine as form3_client
RUN apk add build-base
WORKDIR /app
COPY . .
RUN go mod download
EXPOSE 8080
RUN go test -v -c -o /samplecode_test
CMD ["/samplecode_test", "-test.v"]

#FROM form3interviewapi as build
#CMD ["/form3interviewapi"]





