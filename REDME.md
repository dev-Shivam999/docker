docker ps ->  check the container a run 

docker run -p 3000:3000  img name 

docker build -t img name  .

 docker run -e POSTGRES_PASSWORD=mysecretpassword-d -p 5432:5432 postgres

docker volume create volume name
docker network create network name


docker run -v volume_name:data/db -p 5432:5432  db



full start a db with network and volume :- docker run -d -v volume_name:data/db --name mongo --network networkName  -p 5432:5432 dbName   (mongodb://name:5432/nameOne)



full start a server with network :-  docker run   -p 3000:3000 --name server  --network networkName   imgName




mount:
 docker run -p  3000:3000 -v ./docker_file_in_workingDirectory:/nextapp/app 3000:3000 image_name