
# base image - CampusCore frontend
FROM node:18

# set the working directory
WORKDIR /app

# copy package.json and package-lock.json
COPY package*.json ./

# install dependencies
RUN npm install

# copy the rest of the application code
COPY . .

# build the application
RUN npm run build

# serve the application
RUN npm install -g serve
CMD ["serve", "-s", "build", "-l", "3000"]