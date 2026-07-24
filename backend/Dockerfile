FROM node:20-alpine

# Fixed: the container app directory is now consistent with the project layout.
WORKDIR /app

# Fixed: package files are copied before install to improve layer caching.
COPY package*.json ./
RUN npm install

# Fixed: source files are copied after dependencies are installed.
COPY . .

EXPOSE 5000
CMD ["npm", "start"]