#sequence of each line to understand is important
#container => layer manner
FROM node:24.14.0-alpine

#working directory is /app
WORKDIR /app

#package.json copied into the current dirctory
COPY package*.json ./

#to have node_module ( dont copy node_module directly)
RUN npm install

#copy all remaining
#first dot-> current folder
#second dot-> my container(/app) here
COPY  . .

#for port:http://localhost:5173/
EXPOSE 5173

#to run: npm run dev
#at container level runtime
CMD ["npm" ,"run","dev"]