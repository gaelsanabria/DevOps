FROM node:lts-alpine as hello_world
ENV NODE_ENV=production
WORKDIR /Users/dys0821/DevOps/capstone_project/hello-world
COPY ["package.json", "package-lock.json*", "npm-shrinkwrap.json*", "./"]
RUN npm install --production --silent && mv node_modules ../
COPY . .
EXPOSE 3000
RUN sudo chown -R node /Users/dys0821/DevOps/capstone_project/hello-world
RUN sudo chmod -R 777 *
RUN sudo npm i -g npm; npm i; npm run build
USER node
CMD ["npm", "start"]
