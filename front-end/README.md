![Pushkin Logo](http://i.imgur.com/ncRJMJ5.png)

## Start Your Pushkin Project Locally in Development Mode

1. cd into your main project folder from Terminal
2. From Terminal: `docker-compose -f docker-compose.debug.yml up`
3. When all Docker containers are up and running:

`docker ps`

This gives you a list of the IDs of all Docker containers. Copy the ID of db-worker. 

To seed your database tables with stimuli run:

docker exec -it DB_WORKER_ID bash
npm run migrations
node seeder.js QUIZ_NAME

In your browser go to localhost:8000

Enjoy your website!