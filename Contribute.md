## Manual Installation

- Install Nodejs locally ()
- Clone the repo
- Install the dependencies (npm install)
- Set the scripts in package.json file (start and build)
- Start the DB locally
  - docker run -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
  - Go to neon.tech and get yourself a new DB
- Change the .env file and update your DB credentials
- npx prisma migrate
- npm prisma generate
- npm run build
- npm run start

## Docker Installation

- Install docker
- Start a new network `docker network create user_project`
- Install postgres
  - docker run --network user_project --name postgres -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres
- Build the image - `docker build --network=host -t user-project .`
- Start the image - `docker run -e DATABASE_URL=postgresql://postgres:mysecretpassword@postgres:5432/postgres --network user_project -p 3000:3000 user-project`

## Docker Compose Installation Steps

- Install docker, docker-compose
- Run `docker-compose up`
