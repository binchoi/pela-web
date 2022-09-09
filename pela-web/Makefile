.PHONY: help 

default: help

help:
	@echo 'Management commands for Bin Choi Blog:'
	@echo
	@echo 'Usage:'
	@echo '    make install-hugo           Install Hugo locally.'
	@echo '    make up                     Start the service locally.'
	@echo '    make add-author             Add an author e.g. make add-author name-slug=john.doe'
	@echo '    make create-post       Create a tech post e.g. make create-post post-slug=how-to-python-101'
	@echo

install-hugo: 
	$(call brew install hugo)

up: install-hugo
	@hugo server

add-author: install-hugo
	@hugo new author/$(name-slug).md

create-post: install-hugo
	@hugo new --kind post-bundle blog/$(post-slug)
