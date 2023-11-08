# Build Stage
FROM python:3.9 AS build
WORKDIR /app
COPY app.py .
RUN pip install pyinstaller
RUN pyinstaller --onefile app.py

# Final Stage with Distroless
FROM gcr.io/distroless/python3
WORKDIR /app
COPY --from=build /app/dist/app .
CMD ["./app"]
