# big_data_final_project_133

## producer.py
this function will send the data to consumer

## comsumer.py
it will receive data from producer and will keep the file with batch format

## server.py
to endpoint API, and to run engine and app

## app.py
to setting up routing

## engine.py
initialization, to run the webserver, to call app.py and engine.py, and set the location dataset

total data = 300.000 data/batch
range of time receive = 0.00000000000000001

## model 
1. Model 1: 300.000 first data.
2. Model 2: 300.000 second data.
3. Model 3: 300.000 third data.

## akses API
run localhost (0.0.0.0) with some port

## step by step to run the system
1. run zookeeper with this syntax zkserver<br>
2.make topic in kafka with this syntax
```
kafka-topics.bat — create — zookeeper localhost:2181 — replication-factor 1 — partitions 1 — topic home-kitchen
```
3.run producer.py in spyder<br>
4.run consumer.py spyder<br>
5.after that consumer will receive data<br>
6.run server.py for training data and access API<br>

## API REQUEST
1.give recommendation product according to the user <br>http://localhost:/<model_id>/<user_id>/ratings/top/<count_num>
<br>
![1](./img_pur/6.1.PNG)

2.<br>show the most recommended users by product<br>http://localhost:/<int:model>/products/<int:product_id>/recommend/<int:count>
<br>
![2](./img_pur/6.2.PNG)

3.showing the user rating a particular product<br>http://localhost:/<int:model>/<int:user_id>/ratings/<int:product_id>
<br>
![1](./img_pur/6.3.PNG)

