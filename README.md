# Top level orchestration for cool.gifs

## Usage
1. Create database `.env.db` file
     1. Copy `.env.db.example` to `.env.db`
     1. Change user/password 
1. Create backend .env file
     1. Copy `.env.example` to `.env`
     1. Edit to suit your environment.
     1. Change `SECRET_KEY` to be something unique
     1. Change `CORS_ORIGIN` to be the url to where your frontend will be accessed
     1. Change `SQL_USER` and `SQL_PASSWORD` to match the values in `.env.db`
1. Create frontend .env.frontend` file
     1. Copy `.env.frontend.example` to `.env.frontend`
     1. Change `API_URL` to point to the location of your backend API
1. Edit traefik labels in `docker-compose.yml`
1. Start up the stack `docker-compose up -d`
1. Create a superuser
  `docker exec -it cool-gifs_backend_1 python manage.py createsuperuser`
