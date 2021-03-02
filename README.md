# Hand on Demand

- Hand on Demand was create as a final project while attending Lighthouse Labs

Project by

- Adam Tranquilla - https://github.com/AdamTranquilla
- Natasha Colusso - https://github.com/NColusso
- Zach Harrison - https://github.com/zachharrison

## Description

- Hand on Demand is a fully responsive webapp where users can pin help requests to the map which helpers can filter through & apply to
- When Applying to jobs, helpers can filter based on location, distance, and job category. They can then send a counter offer based on payment type and amount.
- Clicking on a job the map will pan to the location of the job
- Pins on the map are custom based on the category of the job
- When booking a helper clients can message applicants in real time and view there previous jobs reviews before making a decision
- After the completion of a job, clients can review their helper and have the option to mark the job completed, or repost the job which will bring back all pending offers.

## Stack

### Frontend:

- React, JS, CSS, material UI

### Backend:

- Node, express, pSQL, socket.io, google maps API

## Screenshots

!["Screenshot of main page"](https://github.com/NColusso/Hand-on-Demand/blob/master/Screenshots/HoD-Main.png?raw=true)
!["Screenshot of category filter"](https://github.com/NColusso/Hand-on-Demand/blob/master/Screenshots/HoD-Category-Filter.png?raw=true)
!["Screenshot of offering on job"](https://github.com/NColusso/Hand-on-Demand/blob/master/Screenshots/HoD-Offer.png?raw=true)
!["Screenshot of posting job"](https://github.com/NColusso/Hand-on-Demand/blob/master/Screenshots/HoD-Post.png?raw=true)
!["Screenshot of your jobs"](https://github.com/NColusso/Hand-on-Demand/blob/master/Screenshots/HoD-Your-Jobs.png?raw=true)
!["Screenshot of your offers"](https://github.com/NColusso/Hand-on-Demand/blob/master/Screenshots/HoD-Your-Offers.png?raw=true)

## Setup

Install dependencies withing the root, front-end and back-end folder with `npm install`.

## Creating The DB

### On back-end:

1. Use the `psql -U development` command to login to the PostgreSQL server with the username `development` and the password `development`.
2. Create a database with the command `CREATE DATABASE hod_development;`.
3. Copy the `.env.example` file to `.env.development` and fill in the necessary PostgreSQL configuration. The `node-postgres` library uses these environment variables by default.

- this env example should be in the front end and root folder as just .env as well. For convience use the same content for each. You will need to set up your own google maps API key to have the map work as expected.

```
PGHOST=localhost
PGUSER=development
PGDATABASE=hod_development
PGPASSWORD=development
PGPORT=5432

REACT_APP_GOOGLE_API_KEY='PRIVATE KEY'
REACT_APP_MAPBOX_API_KEY='PRIVATE KEY'
FAST_REFRESH=false
CHOKIDAR_USEPOLLING=true
REACT_APP_WEBSOCKET_URL=ws://localhost:8001
PORT=8000
CHOKIDAR_USEPOLLING=false
```

## Seeding the DB

### On back-end:

1. Run a the development server with `npm start` in the Host environment.
2. Then either Make a `GET` request to `/api/debug/reset` with `curl http://localhost:8001/api/debug/reset`, or use the browser to navigate to `http://localhost:8001/api/debug/reset`.

## Run The Server

### On front-end:

1. Run a the server with `npm start`
