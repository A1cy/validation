

# main targets

build: awesome-api	## build the application

run: awesome-api	## run the application
	./awesome-api >>./awesome.log 2>&1 &

stop:	## stop the running application
	@kill "$(shell pgrep awesome-api)" 2>/dev/null && echo "killed" || echo "not running"

clean: stop	## clean build environment
	rm awesome-api awesome.log

test:	## test the application
	curl http://localhost:9999/health

help:	## show this help message
	# needs extra '$' to avoid substitution
	@grep -E '^[a-z].*:.*##.*' Makefile | sed -E 's/^(.*?:).*?## *([a-zA-Z].*)$$/\1 \2/'

# inter

awesome-api: main.go
	go build
