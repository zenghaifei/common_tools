FROM alpine
ENV FRP_VERSION 0.32.1
RUN wget https://github.com/fatedier/frp/releases/download/v${FRP_VERSION}/frp_${FRP_VERSION}_linux_amd64.tar.gz \
    && tar -xf *.gz \
    && mkdir /frp \
    && mv frp_${FRP_VERSION}_linux_amd64/frp* /frp/ \
    && rm -rf frp_${FRP_VERSION}_linux_amd64* \
    && wget https://github.com/zenghaifei/common_tools/raw/master/frps.ini \
    && wget https://github.com/zenghaifei/liberty_infrastructure.frp/raw/master/frpc.ini \
    && mv *.ini /frp/
WORKDIR /frp

EXPOSE 7000 7500 6000
CMD ["./frps", "-c", "./frps.ini"]

