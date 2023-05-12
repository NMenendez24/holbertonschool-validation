## Prerequisites

-A Valid Go-Hugo website is provided

-There are no Git Submodules

-The theme ananke is installed

-No directory dist/ committed

-Makefile present

## Lifecycle

-“build”: compile the source code of the application to a binary named awesome-api

-“clean”: Stop the application. Delete the binary awesome-api and the log file awesome-api.log

-“post”: Create a new blog post whose filename and title come from the environment variables POST_TITLE and POST_NAME.

-“help”: Displays the help for the makefile

-“run”: Run the application in background by executing the binary awesome-api, and write logs into a file named awesome-api.log

-“stop”: Stop the application with the command.

-“test”: Test the aplication with curl

-“lint”: Check for compilation errors in .go files