FROM node:12-alpine
WORKDIR /frontend
ENV PATH /node_modules/.bin:$PATH
ENV NODE_ENV=process.env.NODE_ENV
COPY package*.json ./
RUN npm install
RUN npm install promise
RUN npm install react-scripts@3.4.1
#RUN npm install eslint babel-eslint
EXPOSE 3000
COPY . .
CMD [ "npm", "run", "start" ]

