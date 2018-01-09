.PHONY: ci test clean
MAKEFLAGS = --keep-going

ci: init

init: | test clean

test:
	vagrant up --provision

clean:
	vagrant destroy -f
	rm -rf .vagrant provision.retry
