# Temel Python imajı
FROM python:3.11-slim

# Ortam değişkeni
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Gereksiz cache’leri kapat
RUN pip install --upgrade pip

# Çalışma dizini
WORKDIR /app

# Gereksinimleri yükle
COPY requirements.txt .
RUN pip install -r requirements.txt

# Uygulamayı kopyala
COPY ./app ./app

# Uygulamayı çalıştır
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8000"]

