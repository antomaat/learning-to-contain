FROM alpine AS stage1
RUN echo "Hello World" > /opt/index.html

FROM nginx:alpine
COPY --from=stage1 /opt/index.html /usr/share/nginx/html/
ENTRYPOINT ["nginx", "-g", "daemon off"]
