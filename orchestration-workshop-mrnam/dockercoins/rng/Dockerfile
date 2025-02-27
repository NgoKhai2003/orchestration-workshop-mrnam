
FROM python:alpine

# Cài đặt các gói phụ thuộc cần thiết cho Alpine
RUN apk update && apk add --no-cache \
    bash \
    gcc \
    musl-dev \
    libffi-dev \
    curl

# Cập nhật pip
RUN python -m pip install --upgrade pip

# Cài đặt Flask
RUN pip install Flask --no-cache-dir

# Sao chép mã nguồn vào container
COPY rng.py /app/
WORKDIR /app

# Lệnh khởi chạy ứng dụng
CMD ["python", "rng.py"]

# Mở cổng 80
EXPOSE 80
