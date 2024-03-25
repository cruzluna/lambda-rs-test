# start container

docker run --rm -p 8000:8000 amazon/dynamodb-local

# connect and create a table

aws dynamodb create-table --endpoint-url http://localhost:8000 --table-name Books --attribute-definitions AttributeName=ISBN,AttributeType=S --key-schema AttributeName=ISBN,KeyType=HASH --billing-mode PAY_PER_REQUEST

# list tables

aws dynamodb list-tables --endpoint-url http://localhost:8000

---

# With Docker compose

docker compose up
