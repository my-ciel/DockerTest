FROM nginx:latest
ENV APP_VERSION="1.0.0"
COPY index.html /usr/share/nginx/html/index.html
RUN dd if=/dev/zero of=/usr/share/nginx/html/bigfile bs=1M count=300
RUN echo "temporary file" > /tmp/tmp.txt && rm /tmp/tmp.txt

