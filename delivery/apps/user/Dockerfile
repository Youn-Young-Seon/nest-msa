# 어떤 이미지를 사용할지
FROM node:alpine AS development

WORKDIR /usr/src/app

# package.json 복사하기
COPY package*.json ./

# pnpm-lock.yml
COPY pnpm-lock.yaml ./

# pnpm 설치
RUN npm i -g pnpm

# Dependncy 설치
RUN pnpm i

# 나머지 파일/폴더 복사
COPY . .

# 커맨드 실행
CMD ["pnpm", "start:dev", "user"]
