

build:		## Build the project
	hugo

clean:		## Clean the dist folder
	rm -r dist

post:		## Create a new post
	hugo new posts/${POST_NAME}.md
	sed -i "s/${POST_NAME}/${POST_TITLE}/i" content/posts/${POST_NAME}.md

help:		## Display this help message
	@grep '^[a-z].*##' Makefile | tr -s '\t' ' ' | sed 's/## *//'
