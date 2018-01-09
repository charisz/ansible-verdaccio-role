.PHONY: ci test clean refresh
MAKEFLAGS = --keep-going

ci: | refresh test clean

refresh:
	ansible-galaxy install --roles-path .. --role-file requirements.yml
	vagrant box update

test:
	vagrant up --provision

clean:
	vagrant destroy -f
	rm -rf .vagrant provision.retry
