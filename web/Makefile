VERSION=$(shell git describe --always --dirty)
ORG?=acme
TAG?=latest
build:
	sed -e "s/%%VERSION%%/$(VERSION)/g" < templates/index.html.tmpl > templates/index.html
	docker build -t $(ORG)/web:$(TAG) .
	echo "Built $(ORG)/web:$(TAG)"
