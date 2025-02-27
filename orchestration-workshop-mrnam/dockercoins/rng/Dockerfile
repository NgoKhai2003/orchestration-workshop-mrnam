FROM python:slim

# Cập nhật pip và cài đặt Flask
RUN python -m pip install --upgrade pip
RUN pip install Flask --no-cache-dir

# Cài đặt các gói hệ thống cần thiết nếu cần
RUN apt-get update && apt-get install -y \
    bash \
    gcc \
    libffi-dev \
    curl

# Sao chép mã nguồn vào container
COPY rng.py /app/
WORKDIR /app

# Lệnh khởi chạy ứng dụng
CMD ["python", "rng.py"]

# Mở cổng 80
EXPOSE 80
