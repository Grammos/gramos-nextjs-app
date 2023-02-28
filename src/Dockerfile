FROM node 

# Create app directory
WORKDIR /usr/gramos-nextjs-app

# Install dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
COPY package*.json /usr/gramos-nextjs-app/

RUN npm install

COPY . /usr/gramos-nextjs-app

RUN npm run build

COPY . /usr/gramos-nextjs-app

EXPOSE 3000

ENTRYPOINT [ "npm", "run", "start" ]