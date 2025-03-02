FROM nginx:alpine

ARG USER
ARG GROUP

RUN addgroup -S ${GROUP} && adduser -S ${USER} -G ${GROUP} \
    && chown -R ${USER}:${GROUP} /var/cache/nginx \
    && chown -R ${USER}:${GROUP} /var/run \
    && chown -R ${USER}:${GROUP} /var/log/nginx

EXPOSE 80

USER ${USER}

CMD ["nginx", "-g", "daemon off;"]