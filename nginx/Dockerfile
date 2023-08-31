# bundle static assets with nginx
FROM nginx:1.21.0-alpine as production
ENV NODE_ENV production

# remove existing files from nginx directory
RUN rm -rf /usr/share/nginx/html/*

# add nginx config
COPY nginx.conf /etc/nginx/conf.d/default.conf

# expose port 80 for nginx
EXPOSE 80

# start nginx
CMD ["nginx", "-g", "daemon off;"]
