FROM python:alpine
RUN pip install Flask --no-cache-dir
COPY rng.py /
CMD ["python", "rng.py"]
EXPOSE 80
