## Install all dependencies

```bash
yarn install
```

## Setting up local PostgreSQL database

Open your pgAdmin, then go to your servers and find PostgreSQL (version).
Create a new database (input your own database name).
Once created, you may proceed to the next part of this file.

## Create .env files

Create a .env file in the root of your project directory where the prisma folder is located, and paste this inside it.

```bash
DATABASE_URL="postgresql://username:password@host:port/database_name?options";
```

Please replace 
```bash
username, 
password, 
host, 
port, 
database_name, and 
options
```
with your actual PostgreSQL database credentials and details.

## Prisma client

To refresh Prisma client (if Prisma is not loading correctly),

```bash
npx prisma generate
```

then after,

```bash
npx prisma migrate dev --name init
```

to apply database migration to your local PostgreSQL database.

## Run the program / test

```bash
yarn dev
```

```bash
yarn test
```