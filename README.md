# mysql_reverse_replication
This is the reverse replication from mysql 8.0.35 > 5.7.44 > 5.6.51

You can run this using 
docker compose up -d

If you want to stop
docker compose down
Step 1 :- Download the repo

Step 2 :- Start docker compose
          
          docker compose up -d
          
Step 3 :- Check if all the containers are running
          
          docker ps
          
Step 4 :- Exec into 8.0 container to get "SHOW MASTER STATUS"

          docker exec -it $container_id_8.0 bash
          
Step 4 :- Exec into 5.7 container and Execute CHANGE MASTER
          
          docker exec -it $container_id_5.7 bash
          
Step 5 :- Repeat above step for 5.6

Step 6 :- Test the replication creating some data.
