GO_VERSION := 1.19.6
GO_PLATFORM := linux-amd64

setup:
	install-go
	init-go

install-go:
	wget "https://golang.org/dl/go$(GO_VERSION).$(GO_PLATFORM).tar.gz"
	sudo tar -C /usr/local -xzf go$(GO_VERSION).$(GO_PLATFORM).tar.gz
	rm go$(GO_VERSION).$(GO_PLATFORM).tar.gz

init-go:
	echo 'export PATH=$$PATH:/usr/local/go/bin' >> $${HOME}/.bashrc
	echo 'export PATH=$$PATH:$${HOME}/go/bin' >> $${HOME}/.bashrc

upgrade-go:
	sudo rm -rf /usr/bin/go
	wget "https://golang.org/dl/go$(GO_VERSION).$(GO_PLATFORM).tag.gz"
	sudo tar -C /usr/local -xzf go$(GO_VERSION).$(GO_PLATFORM).tar.gz
	rm go$(GO_VERSION).$(GO_PLATFORM).tar.gz

build:
	go build -o api cmd/main.go


