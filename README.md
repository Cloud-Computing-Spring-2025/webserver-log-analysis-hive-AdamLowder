# Web-Server-Log-Analysis

For this in class assignment we loaded web_server_logs.csv into our docker container before then moving it to a hive iput folder where we were able to begin running queries in hue to get the results we are looking for. Below are the steps used to do this.

1. compose docker up -d : to copy over the necassary docker files.

2. docker cp web_server_logs.csv hive-server./ : copy csv to container

3. docker exec -it hive /bin/bash : move into hive terminal

4. hdfs dfs -mkdir /input : make input folder

5. hdfs dfs -put ./web_server_logs.csv /input : place csv in correct input folder

6. Now we can begin running our hue queries. I have linked all of the screenshots ad results of each query in the attached google doc.