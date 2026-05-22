FROM python:3.12-slim

WORKDIR /app


RUN apt-get update && apt-get install -y curl

RUN pip install --no-cache-dir flask

RUN useradd -m appuser
RUN chown -R appuser:appuser /app

# Switch to non-root user
USER appuser


COPY app.py .

CMD ["python", "app.py"]