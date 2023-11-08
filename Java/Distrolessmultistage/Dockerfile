# Build Stage
FROM openjdk:11 AS build
WORKDIR /app
COPY Main.java .
RUN javac Main.java

# Final Stage with Distroless
FROM gcr.io/distroless/java:11
WORKDIR /app
COPY --from=build /app/Main.class .
CMD ["Main"]
