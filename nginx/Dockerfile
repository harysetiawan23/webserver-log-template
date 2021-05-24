FROM nginx:stable-alpine

WORKDIR /nginx
COPY ./conf /nginx/conf

CMD ["nginx", "-c", "/nginx/conf/nginx.conf"]