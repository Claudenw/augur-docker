# To Deploy a new version of the containers: 
1. Clone and build https://github.com/chaoss/augur
2. Build and Run the Augur Docker containers locally
3. Tag and push, replacing the container hash with the results of the first command mapped to the correct container name: 
```{eval-rst} 
docker container ls
docker tag ec43be8f296a augurlabs/augur-redis-1
docker tag 715acd0b3971 augurlabs/augur-augur-db-1
docker tag e94d30912c06 augurlabs/augur-rabbitmq-1
docker tag 21c60a10ab9f augurlabs/augur-augur-1
docker push augurlabs/augur-redis-1 
docker push augurlabs/augur-augur-db-1
docker push augurlabs/augur-rabbitmq-1
docker push augurlabs/augur-augur-1
```