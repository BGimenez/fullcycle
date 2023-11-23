#Create image to build project
FROM golang:1.21 AS build

#Create directory
WORKDIR /usr/src/app

#Copy module file from locale to container
COPY /app/go.mod ./
#Necessary to compile project
RUN go mod download && go mod verify

#Copy project file from locale to container
COPY /app/hello.go .

#Execute build to project
RUN GOOS=linux go build hello.go

# Final image
#Create image linux
FROM scratch

#Create directory
WORKDIR /app

#Copy project files builded from previous image
COPY --from=build /usr/src/app ./

#Execute project
CMD ["./hello"]
