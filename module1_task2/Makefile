build: ## Builds the site
	@hugo

clean: ## Cleans the dist folder
	@rm -rf dist

post: ## Creates a new post with the name and the title given
	@hugo new posts/$(POST_NAME).md
	@echo "---\ntitle: '$(POST_TITLE)'\ndate: $$(date +"%Y-%m-%dT%H:%M:%S%z")\n---" > content/posts/$(POST_NAME).md

help: ## Show this help usage
	@awk -F ': ## ' '/^[^\.%\t][a-zA-Z0-9._-]+:.*##/ { printf "%s: \033[0m %s\n", $$1, $$2 }' $(MAKEFILE_LIST)