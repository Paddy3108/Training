FROM docker:dind

WORKDIR /usr

COPY git_shell.sh .

RUN apk add --no-cache git \
	&& chmod +x /usr/git_shell.sh
	
CMD ["/bin/ash", "/usr/git_shell.sh"]