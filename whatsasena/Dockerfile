FROM fusuf/whatsasena:latest

RUN git clone https://github.com/whiteshadowofficial/Lasa /root/4IDTS
WORKDIR /root/WhatsAsena/
ENV TZ=Europe/Istanbul
RUN npm install supervisor -g
RUN git clone https://github.com/whiteshadowofficial/files
RUN apk --no-cache --virtual build-dependencies add \
    python \
    make \
    g++ \
    && npm install \
    && apk del build-dependencies
RUN npm install

CMD ["node", "bot.js"]
