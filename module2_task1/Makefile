build: lint ## Builds and run the site
	@go build -o awesome-api

clean: ## Cleans the api and logs
	@rm ./awesome-api ./awesome-api.log

post: ## Creates a new post with the name and the title given
	@hugo new posts/$(POST_NAME).md
	@echo "---\ntitle: '$(POST_TITLE)'\ndate: $$(date +"%Y-%m-%dT%H:%M:%S%z")\n---" > content/posts/$(POST_NAME).md

help: ## Show this help usage
	@awk -F ': ## ' '/^[^\.%\t][a-zA-Z0-9._-]+:.*##/ { printf "%s: \033[0m %s\n", $$1, $$2 }' $(MAKEFILE_LIST)

run: ## Runs the api
	@./awesome-api >./awesome-api.log 2>&1 &

stop: ## Stops the api
	@pkill awesome-api

test: ## Tests the api
	@curl http://localhost:9999
	@curl http://localhost:9999/health

lint: ## Checks for compilation errors
	@golangci-lint run
