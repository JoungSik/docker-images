# Docker images

이 레포지토리는 로컬에서 사용하는 Docker 이미지들을 모아놓은 프로젝트입니다. `.env` 파일에서 `DATA_DIR` 키를 통해 데이터를 저장할 디렉토리를 설정할 수 있으며, 간단한 설정만으로 Docker 환경을 구성할 수 있습니다.

## 시작하기

### 1. 클론 및 디렉토리 이동

레포지토리를 클론한 후 해당 디렉토리로 이동합니다:

```bash
git clone https://github.com/joungsik/docker-images
cd docker-images
```

### 2. `.env` 파일 생성 및 설정

레포지토리 루트에 `.env` 파일을 생성하고 다음 내용을 추가합니다:

```
DATA_DIR=/path/to/your/data-directory
```

`/path/to/your/data-directory`를 실제 데이터가 저장될 디렉토리로 변경하세요.

### 3. Docker Compose 실행

아래 명령어로 Docker Compose를 실행하여 컨테이너를 시작합니다:

```bash
docker-compose up -d
```

### 4. 데이터 디렉토리 확인

`DATA_DIR`로 설정한 경로에 데이터 폴더가 생성됩니다. 해당 디렉토리에서 컨테이너에 의해 저장된 데이터를 확인할 수 있습니다.

## 구성된 서비스

이 레포지토리는 다음과 같은 Docker 이미지를 포함하고 있습니다:

- postgres:16

## 종료하기

컨테이너를 중지하려면 아래 명령어를 실행하세요:

```bash
docker-compose down
```

## 주의사항

- `DATA_DIR` 경로는 반드시 로컬 머신에서 접근 가능한 디렉토리여야 합니다.
- 기존 데이터를 유지하려면 `docker-compose down` 시 데이터 디렉토리를 삭제하지 마세요.

## 문의

프로젝트와 관련된 문의사항은 이슈를 생성하거나 [tjstlr2010@gmail.com]로 연락주세요.
