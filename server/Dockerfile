FROM node:16.20.2-alpine
WORKDIR /usr/src/app
RUN adduser -D mern-user
COPY package*.json ./
RUN npm install 
COPY --chown=mern-user:mern-user . .
COPY --chown=mern-user:mern-user .env ./
USER mern-user
EXPOSE 3000
CMD ["npm", "start"]
