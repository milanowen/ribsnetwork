#
# Dockerfile for xware
#

FROM debian:wheezy-slim
MAINTAINER cuteribs <ericfine1981@live.com>

WORKDIR /xware

COPY ./*.deb /xware/
ADD ./xware.tar.bz /xware/

RUN	dpkg -i /xware/libc6-*.deb && \
	dpkg -i /xware/lib32z1_*.deb && \
	chmod +x /xware/portal && \
	rm /xware/*.deb

CMD /xware/portal > /xware/portal.log 2>&1 && tail -f /xware/portal.log