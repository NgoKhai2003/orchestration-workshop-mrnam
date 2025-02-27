FROM python:alpine
ENV http_proxy=http://proxy.example.com:8080
ENV https_proxy=http://proxy.example.com:8080

# Cài đặt các chứng chỉ SSL cần thiết
RUN apk add --no-cache ca-certificates

# Cập nhật pip lên phiên bản mới nhất
RUN python -m pip install --upgrade pip
RUN ping -c 4 google.com
# Cài đặt Flask
RUN pip install Flask --no-cache-dir

# Sao chép mã nguồn vào container
COPY rng.py /

# Chạy ứng dụng Python
CMD ["python", "rng.py"]
