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
Step 4 :- Exec into 5.7 container and Execute CHANGE MASTER command using "SHOW MASTER STATUS" from the mysql 8.
          docker exec -it $container_id bash
Step 5 :- Repeat same for 5.6
Step 6 :- Test the replication creating some data.
