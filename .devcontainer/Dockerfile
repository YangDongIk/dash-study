FROM python:3.11-slim

# 시스템 패키지 업데이트 및 Git 설치
RUN apt-get update && apt-get install -y \
    git \
    build-essential \
    curl \
    && rm -rf /var/lib/apt/lists/*

# 작업 디렉토리 설정
WORKDIR /app

# 의존성 복사 및 설치
COPY .devcontainer/requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Dash 앱 포트
EXPOSE 8050

CMD ["sleep", "infinity"]
