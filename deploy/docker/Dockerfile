FROM nginx:1.17.4-alpine
#FROM nginx:1.17

COPY nginx.conf /etc/nginx/nginx.conf
COPY default.conf /etc/nginx/conf.d/default.conf
COPY dist /usr/share/nginx/web

RUN chown -R nginx /usr/share/nginx/

EXPOSE 3030