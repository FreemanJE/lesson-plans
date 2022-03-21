# GIT

- is a software versioning tool
- every `git commit` has
    - a message
    - a commit hash - a unique id which identifies that commit
- we can use `.gitignore` to reference files or folders that we want git to ignore
    > Create it first before adding files to your project!
- [gitignore generator](https://www.toptal.com/developers/gitignore). Use keywords depending on environment, OS (operating system), IDE (integrated development environment)
    - Visual Studio Code
    - WebStorm
    - Windows
    - Linux
    - OSX
    - dotenv
    - Node
- `git rm --cached .env`
- `git rebase` - strike fear into developers!
- checkout to latest commit `git checkout {branchname}`
- `git checkout -b {branchname}` will create a new branch (copy)

# Nodemon

[https://github.com/remy/nodemon](https://github.com/remy/nodemon)

- an alternative to using `node`
- it is optional
- it consumes the terminal while it is running (you cannot run anything else)
- it listens for changes to the files you've executed
- it re-runs the application after you've hit save

# Servers

Servers are not so much the computers themselves, but the processes running on them

- listening for a client connection (request)
- responds to the client request

# Examples of clients

- browser
- API testing tool (postman, insomnia)
- mobile phone
- also, another server

# Request types

## GET request

- we just want to "GET" data from the server
- it's the simplest of all requests
- when we visit a website, we are actually making a GET request to "GET" the html on the page
- we can make a GET request using the address bar in the browser

## POST request

- we use this type of request to send data to the server
- we CANNOT make a POST request using the address bar in the browser

