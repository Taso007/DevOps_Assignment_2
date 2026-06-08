# Small instrumented Express application
FROM node:20-alpine

WORKDIR /usr/src/app

# Install dependencies first so Docker can cache this layer
COPY package*.json ./
RUN npm install --omit=dev

# Copy application source
COPY src ./src

EXPOSE 3000

CMD ["node", "src/index.js"]
