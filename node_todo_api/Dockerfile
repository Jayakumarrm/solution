FROM node:8.11.3-alpine

WORKDIR /app

# Copy package.json file
COPY package.json package.json

#  Install node_modules
RUN npm install

# Copy application's folders and files
COPY app.js app.js
COPY ./api ./api
COPY ./config ./config
COPY ./assets ./assets
COPY ./tasks ./tasks
COPY ./test ./test
COPY ./views ./views
COPY ./Gruntfile.js ./Gruntfile.js
COPY ./.sailsrc ./.sailsrc
COPY ./.eslintrc.json ./.eslintrc.json

RUN mkdir .tmp
RUN chmod +x .tmp

EXPOSE 1337
CMD ["npm", "start"]