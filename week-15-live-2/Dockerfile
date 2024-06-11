# This is a brute force dockerfile
# FROM node:20

# WORKDIR /app

# COPY . .

# RUN npm install
# RUN npx prisma generate
# RUN npm run build

# EXPOSE 3000

# CMD ["node", "dist/index.js"]

# This is optimised dockerfile. In the above approach we are runninn npm install everytime the files changes. Do we really need it ? 
# No !. Not at all. so we can just follow this to skip running npm install when there is no change in packege.json

FROM node:20

WORKDIR /app

COPY package* .
COPY ./prisma .

RUN npm install
RUN npx prisma generate

EXPOSE 3000

CMD [ "node", "dist/index.js"]

