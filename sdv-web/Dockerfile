# FROM node:23.0.0 as builder

# WORKDIR /usr/src/app

# COPY package*.json ./

# RUN npm install

# COPY . .

# RUN npm run build

# # # For PROD
# # FROM node:23.0.0-alpine

# # WORKDIR /usr/src/app

# # COPY --from=builder /usr/src/app/package*.json ./

# # RUN npm install --only=production

# # COPY --from=builder /usr/src/app/dist ./

# # EXPOSE 3000

# # CMD ["node", "server.js"]

# # Keep Alive
# CMD [ "tail", "-f", "/dev/null" ]
