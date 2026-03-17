FROM sbs20/scanservjs:latest

# Install brscan4
RUN apt-get update && apt-get install -y curl

RUN curl -O https://download.brother.com/welcome/dlf105200/brscan4-0.4.11-1.amd64.deb \
 && dpkg -i brscan4-0.4.11-1.amd64.deb \
 && brsaneconfig4 -a name=Brother model=MFC-L2710DW ip=10.0.50.180 \
 && rm brscan4-0.4.11-1.amd64.deb