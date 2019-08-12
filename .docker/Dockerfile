FROM 	httpd:2.4

LABEL   maintainer="Frederick Tyteca"

# setting timezone
ENV     TZ=Europe/Paris
RUN     ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone
