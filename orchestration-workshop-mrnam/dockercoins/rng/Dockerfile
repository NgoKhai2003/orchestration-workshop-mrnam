FROM python:alpine
RUN python -m pip install --upgrade pip
RUN pip install Flask
COPY rng.py /
CMD ["python", "rng.py"]
EXPOSE 80

