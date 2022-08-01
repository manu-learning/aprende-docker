FROM alpine:edge

RUN apk update
RUN apk add weechat-matrix git make py3-pip

WORKDIR /tmp/weechat-matrix
RUN git clone https://github.com/poljar/weechat-matrix.git .
RUN pip install --user -r requirements.txt
RUN make install
RUN mkdir -p ~/.weechat/python/autoload && ln -s ~/.weechat/python/matrix.py ~/.weechat/python/autoload/ 

CMD ["weechat"]