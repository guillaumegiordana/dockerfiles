FROM		debian:stable
LABEL		CMDBUILD="docker build -t giorg/samba https://raw.githubusercontent.com/guillaumegiordana/dockerfiles/master/samba/Dockerfile"
LABEL		CMDRUN="docker run giorg/samba"

MAINTAINER	Guillaume Giordana <guillaume.giordana@gmail.com> 

# gettext for envsubst
RUN		apt-get update && \
			apt-get install -yq samba gettext
ADD		share.tmpl /share.tmpl
ADD		setup.sh /setup.sh

ENTRYPOINT      ["/setup.sh"]
