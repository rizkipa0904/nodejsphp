FROM node:13
COPY . . /

RUN npm install
RUN npm install pm2 -g

CMD ["pm2-runtime", "index.js"]

EXPOSE 3000
