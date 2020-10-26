# Task Manager
## Users
- POST /users
  - Signs in a new user and stores it in the db if a valid body was provided
- POST /users/login
  - Logins if valid credentials were provided
- POST /users/logout
  - Logouts the current user
- POST /users/logout
  - Logouts the current user from the current instance
- POST /users/logoutAll
  - Logouts the current user from all instances
- GET /users/me
  - Reads your profile
- PATCH /users/me
  - Updates your profile if you were authenticated and provided valid data
- DELETE /users/me
  - Deletes your user
- POST /users/me/avatar
  - Uploads an avatar image
- DELETE /users/me/avatar
  - Deletes your avatar
- GET /users/:id/avatar
  - Shows the avatar from the user with the specified id

User Entity:
  - Name: string
  - Email: boolean
  - Password: string
  - Age: number
  - Avatar: image
  
  ## Tasks
- GET /tasks
  - Returns the list of saved tasks
- GET /tasks/:id
  - Returns the tasks with specified id. If not found, it returns 404NOTFOUND error
- POST /tasks
  - Creates a new task in the DB
- UPDATE /tasks/:id
  - Updates the task with the specified id with the body content if data is valid
- DELETE /tasks/:id
  - Deletes the task with the specified id

Task Entity:
  - Description: string
  - Finished: boolean


## Instructions to setup dev environment
Create "dev.env" file in /config

You will need to set 3 fields in the file:

`
SENDGRID_API_KEY=yourkey // your SendGrid API key for sending e-mails
`

`
JWT_SECRET=yoursecret // your JWT secret for creating tokens, don't share this
`

`
MONGODB_URL=yoururl // your MongoDB database url
`

Please do the same thing for /config/test.env.

After that you should be able to run `npm install` to install all the dependencies.

You can read the package.json to see the commands you can run in the project.
