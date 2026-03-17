FROM sbs20/scanservjs:latest

ARG TARGETARCH

# Install brscan4
RUN apt-get update && apt-get install -y curl

RUN if [ "$TARGETARCH" = "arm64" ]; then \
      curl -O https://download.brother.com/welcome/dlf105200/brscan4-0.4.11-1.arm64.deb \
      && dpkg -i brscan4-0.4.11-1.arm64.deb \
      && rm brscan4-0.4.11-1.arm64.deb; \
    else \
      curl -O https://download.brother.com/welcome/dlf105200/brscan4-0.4.11-1.amd64.deb \
      && dpkg -i brscan4-0.4.11-1.amd64.deb \
      && rm brscan4-0.4.11-1.amd64.deb; \
    fi \
 && brsaneconfig4 -a name=Brother model=MFC-L2710DW ip=10.0.50.180