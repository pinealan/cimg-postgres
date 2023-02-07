# vim:set ft=dockerfile:

FROM cimg/postgres:13.9

LABEL maintainer="Alan Chan"
ENV PGTAP_VERSION v1.2.0

RUN apt-get update && apt-get install -y --no-install-recommends \
	git \
	make \
	perl \
	&& \
	rm -rf /var/lib/apt/lists/* && \
	git clone https://github.com/theory/pgtap.git && \
	cd pgtap && \
	git checkout tags/$PGTAP_VERSION && \
	make && \
	make install
