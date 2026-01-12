# n8n Docker Compose 실행

n8n을 로컬에서 빠르게 실행할 수 있도록 Docker Compose 설정을 제공합니다.

## 필요 조건
- Docker 및 Docker Compose v2

## 실행 방법
1. 컨테이너 시작: `docker compose up -d`
2. 브라우저에서 `http://localhost:5678` 접속 (기본 포트 5678)
- 사용 이미지는 `n8nio/n8n:1.80.1`로 고정되어 있으며 필요 시 `docker-compose.yml`에서 버전을 조정하세요.

## 볼륨
- `n8n_data` → `/home/node/.n8n` (워크플로, 자격 증명, 기본 DB/설정 및 로그 보존)

## 정리 및 로그
- 로그 확인: `docker compose logs -f n8n`
- 컨테이너 중지: `docker compose down`
- 데이터를 포함해 초기화: `docker compose down -v`
