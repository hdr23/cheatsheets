FROM node:25-alpine

WORKDIR /usr/src/app

COPY package.json ./

RUN npm install --verbose

COPY . .

# Vite defaults to port 5173
EXPOSE 5173

# We add the '--host' flag so the app is accessible outside the container
CMD ["npm", "run", "dev", "--", "--host"]