FROM node:latest as node
WORKDIR /app
COPY. .
RUN npm instakk
RUN npm run build --prod

FROM nginx:alpine
COPY --from =node /app/dist/angular-app