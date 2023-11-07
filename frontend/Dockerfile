From node:16.14.2 as build

#Build the frontend
WORKDIR /app


COPY . .
RUN npm i

RUN npm run build

From nginx:latest

COPY --from=build /app/build /etc/nginx/html