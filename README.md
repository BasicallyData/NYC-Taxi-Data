# NYC-Taxi-Data
Ingesting NYC taxi data

ls - to list file path
cd 2_docker_sql <- to enter filepath

docker run -it \
  -e POSTGRES_USER="root" \
  -e POSTGRES_PASSWORD="root" \
  -e POSTGRES_DB="ny_taxi" \
  -v $(pwd)/ny_taxi_postgres_data:/var/lib/postgresql/data \
  -p 5432:5432 \
  postgres:13


pgcli -h localhost -p 5432 -u root -d ny_taxi

postgresql:
\dt list tables
\d describe table schema
