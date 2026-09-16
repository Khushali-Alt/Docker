# from where i should start
#use an official image of NOde.js runtime
FROM node:24.14.0-alpine

#set the working directory inside the container
#current directory is /app 
WORKDIR  /app

#copy all package.json files in working directory
COPY package*.json ./

#install dependencies
RUN npm install

#copy all the file into currenctly container working directory
#its also bring node module file-> learn it to not
COPY . .

ENV PORT=3000

EXPOSE 3000

CMD ["npm" , "start"]