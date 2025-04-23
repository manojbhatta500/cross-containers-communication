FROM node:22

WORKDIR /backend

COPY  ./package.json /backend/

RUN npm install

COPY . /backend 


ENV USERNAME=user

ENV PASSKEY=secret

EXPOSE 8080

CMD [ "npm","start" ]

