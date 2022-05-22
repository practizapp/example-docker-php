usage:
	@echo "Available targets:"
	@echo "  * build               - Builds image"
	@echo "  * create-project      - Runs bundle install & create new symphony project"
	@echo "  * up                  - Running all Container"
	@echo "  * down                - Removes all the containers"
	@echo "  * restart             - restart all the containers"
	@echo "  * destroy             - Removes all the containers with volumes and tears down the setup"
up:
	docker compose up -d
down:
	docker compose down --remove-orphans
build:
	docker compose build --no-cache --force-rm
create-project:
	mkdir app
	@make build
	@make up
	docker compose exec php symfony new .
destroy:
	docker compose down --rmi all --volumes --remove-orphans
restart:
	@make down
	@make up
