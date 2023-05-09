build:
	@hugo

clean:
	@rm -rf dist

post:
	@hugo new posts/$(POST_NAME).md
	@echo "---\ntitle: '$(POST_TITLE)'\ndate: $$(date +"%Y-%m-%dT%H:%M:%S%z")\n---" > content/posts/$(POST_NAME).md