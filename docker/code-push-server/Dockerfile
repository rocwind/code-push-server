FROM node:8.17.0-alpine

RUN npm config set registry https://registry.npm.taobao.org/ \
&& npm i -g code-push-server@0.5.2 pm2@latest --no-optional

COPY ./process.json /process.json

EXPOSE 3000

CMD ["pm2-docker", "start", "/process.json"]
