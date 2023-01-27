# here we are writting multi stage docker file because to to build the code we need maven
FROM node:14
WORKDIR /app
COPY . .
RUN npm install
EXPOSE 1004
CMD ["node","index.js"]

