FROM python:alpine

# Cài đặt các gói phụ thuộc cần thiết cho Alpine (bao gồm curl, gcc, v.v.)
RUN apk update && apk add --no-cache \
    bash \
    gcc \
    musl-dev \
    libffi-dev \
    curl

# Cập nhật pip và cài đặt Flask
RUN python -m pip install --upgrade pip
RUN pip install Flask

# Sao chép mã nguồn vào container
COPY rng.py /app/
WORKDIR /app

# Khởi chạy ứng dụng
CMD ["python", "rng.py"]

# Mở cổng 80
EXPOSE 80

