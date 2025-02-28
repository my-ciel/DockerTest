# 베이스 이미지 설정 (Slim 버전 활용)
FROM python:3.12-slim

# 작업 디렉토리 설정
WORKDIR /app

# 필요한 패키지 설치를 위해 종속성 파일 복사 (캐시 활용)
COPY requirements.txt .

# 패키지 설치 (캐시 최적화)
RUN pip install --no-cache-dir -r requirements.txt

# 애플리케이션 소스 코드 복사
COPY . .

# Flask 실행을 위한 환경 변수 설정
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0
ENV FLASK_RUN_PORT=5000

# 기본 실행 명령 (flask run 대신 Gunicorn을 사용하는 것도 고려 가능)
CMD ["python", "app.py"]
