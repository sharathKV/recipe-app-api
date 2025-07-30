# recipe-app-api
Recipe API project

This is a Django Project built using TDD methodology. The application provides APIs for creating, updating and deleting recipes. APIs are also provided for adding ingredients and tags to recipes which can then be used to filter the recipes. The application is also docker containerized and configurations are added to make it production ready. I've also tried to demonstrate some of the CI methodologies by ensuring linter and tests are run every time changes are committed to this repo through GitHub actions.

To test the application locally, Git, Docker and Docker Compose tools are required.

1. Git clone the repository to your local workspace
2. run `docker-compose run --rm app sh -c "python manage.py test"` to check if all the relevant dependencies are installed and the unit tests are passing.
3. run `docker-compose run --rm app sh -c "python manage.py runserver"`

Headover to http://127.0.0.1:8000/api/doc which opens up the swagger doc.

The application uses a token based authentication mechanism, hence first create the user and use the token api to get the token. Authorize the APIs using the generated token.
