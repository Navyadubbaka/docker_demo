FROM python:3.12 AS builder
WORKDIR /build
COPY app.py .

FROM python:3.12-slim
WORKDIR /app
COPY --from=builder /build/app.py .
CMD ["python3", "app.py"]

