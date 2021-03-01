FROM node:14-alpine
WORKDIR /frontend
ENV PATH /node_modules/.bin:$PATH
ENV BABEL_ENV=development
ENV NODE_ENV=development
ENV require=./config/env
ENV process.on=unhandledRejection
COPY package*.json ./
#Dependencias necesarias
#RUN npm install react-scripts@3.4.1
#RUN npm install promise -g
#RUN npm install babel -g
#RUN npm install webpack webpack-dev-server -g
RUN npm install --production
EXPOSE 3000
COPY . .
CMD [ "npm", "start" ]

