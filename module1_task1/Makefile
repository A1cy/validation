

build:
	hugo

clean:
	rm -r dist

post:
	hugo new posts/${POST_NAME}.md
	sed -i "s/${POST_NAME}/${POST_TITLE}/i" content/posts/${POST_NAME}.md
