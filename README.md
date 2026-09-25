# postman-test

A repo for Postman collections and environment files

## Repo Clone and Submission

Please clone this repo (do NOT fork it), and push changes to your own account. Example of process steps linked [here](https://stackoverflow.com/questions/18200248/cloning-a-repo-from-someone-elses-github-and-pushing-it-to-a-repo-on-my-github).

```
- Follow good version control practices.
- An initial commit after cloning the repo, before making any changes.
- Any additional commits you want as you progress through the task.
```

Please push your work to your own github repo and share the link to the project with us, in good time, for review prior to interview. Please expect some questions/technical discussion during the interview, relating to your implementation of the given task.

## Project Requirements / Recommendations

- GitHub Account
- Postman Account

# Required task

There is a mock API available, details:

URI : http://dev-unity-uks-test-mock-api.uksouth.azurecontainer.io:3000 with the endpoints:
- POST /token
- GET /users
- GET /users/{userId}
- POST /users
- PUT /users
- DELETE /users/{userId}

POST\PUT users schema:
```
{
	"type": "object",
	"properties": {
		"name": {
			"type": "string",
			"minLength": 1
		},
		"email": {
			"type": "string",
			"minLength": 1
		},
		"nickName": {
			"type": "string",
			"minLength": 0
		}
	},
	"required": [
		"name",
		"email"
	]
}
```
Additional information:
- The POST /token request uses Basic Auth
	- Username: Admin123
	- Password: pw0rD!123456
- Other endpoints require Bearer token authentication.
- There is no data layer, any changes made to entities are not retained.

Please create a Postman collection containing tests to cover each API and a supporting environment file.

Please submit your own code, NOT AI generated solutions to the problem.
