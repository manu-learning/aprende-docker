all: run shell

run:
	@docker-compose up -d

shell:
	@docker-compose exec -it weechat weechat

stop:
	@docker-compose stop

rm:
	@docker-compose down

.PHONY: run shell stop rm
