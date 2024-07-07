# Microservice communication with RabbitMQ
Producer:

docker build -t producer-image -f producer/Dockerfile .
Consumer One:

docker build -t consumer-one-image -f consumer_one/Dockerfile .
Consumer Two:

docker build -t consumer-two-image -f consumer_two/Dockerfile .
Consumer Three:

docker build -t consumer-three-image -f consumer_three/Dockerfile .
Consumer Four:

docker build -t consumer-four-image -f consumer_four/Dockerfile .

individual build step and correct command structure.
After building the images, you can run the application using Docker Compose. Update your docker-compose.yml to use these images:

push
# Log in to Docker Hub
docker login

# Push the images to Docker Hub
docker tag producer-image bharathoptdocker/python-producer
docker push bharathoptdocker/python-producer

docker tag consumer-one-image bharathoptdocker/python-consumer-one
docker push bharathoptdocker/python-consumer-one

docker tag consumer-two-image bharathoptdocker/python-consumer-two
docker push bharathoptdocker/python-consumer-two

docker tag consumer-three-image bharathoptdocker/python-consumer-three
docker push bharathoptdocker/python-consumer-three

docker tag consumer-four-image bharathoptdocker/python-consumer-four
docker push bharathoptdocker/python-consumer-four
```
