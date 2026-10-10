FROM nginx:1.17.4-alpine

COPY deploy/docker/nginx.conf /etc/nginx/nginx.conf
COPY deploy/docker/default.conf /etc/nginx/conf.d/default.conf

# dist 由GitHub Action流水线提前生成在runner主机，直接复制进镜像
COPY dist /usr/share/nginx/web

RUN chown -R nginx /usr/share/nginx/
EXPOSE 3030
CMD ["nginx", "-g", "daemon off;"]