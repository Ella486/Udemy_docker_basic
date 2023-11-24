#도커 파일 시작

# NodeJS 기본 이미지 사용 - 컨테이너 내부에서 NodeJS 사용
FROM node:14  

# 컨테이너 파일 시스템 내 특정 디렉토리
WORKDIR /app

# package.json 파일을 작업 디렉토리에 복사
COPY package.json .

# npm install 명령어를 실행해서 애플리케이션에 필요한 모든 종속성을 설치
RUN npm install

# 그런 다음 나머지 코드를 여기에 복사
COPY . .

# 포트 3000d을 외부로 노출
EXPOSE 3000

# node 명령으로 app.mjs 실행
CMD [ "node", "app.mjs" ]