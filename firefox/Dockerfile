FROM alpine:latest

ENV URL https://www.google.com

RUN apk --no-cache --update add firefox-esr dbus-x11 ttf-freefont \
    && adduser -S jelou \
    && echo "jelou:jelou" | chpasswd

USER jelou

CMD firefox --new-instance ${URL}