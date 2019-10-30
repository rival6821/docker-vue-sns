FROM node:10

# app 폴더 만들기
RUN mkdir -p /app

# work dir 설정
WORKDIR /app

# 서버파일 복사
COPY package.json /app
COPY package-lock.json /app

# 패키지파일들 받기
RUN npm install

COPY . /app
# 배포버전으로 설정
ENV NODE_ENV=production

#서버실행
CMD ["npm","run","dev"]
