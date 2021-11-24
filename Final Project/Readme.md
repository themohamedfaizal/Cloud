# Design a Highly Avaiable Web application


### Architechture overview

![image](https://user-images.githubusercontent.com/91851332/143187836-99cbeb32-2f85-4533-ad4b-6b6152419930.png)


### 1. Creating a VPC - ( 10.0.0.0/16)

![image](https://user-images.githubusercontent.com/91851332/143185212-3415fbea-81f5-4b3e-9a86-dbd9de06282e.png)


### 2. Creating 4 subnets - (10.0.0.0/24)

![image](https://user-images.githubusercontent.com/91851332/143185453-147eabdb-8945-436b-9b38-a600f97215dd.png)


### 3. Create RouteTable - 1 for Webserver and 1 for Database Server

![image](https://user-images.githubusercontent.com/91851332/143186842-58162c8f-da3b-4ea4-9fc4-75822e90d3d4.png)


### 4. Creating IGW for Outside access and Attaching it to WebServer Route table.

![image](https://user-images.githubusercontent.com/91851332/143187319-1d113d53-3490-48d4-9f53-70c13cb683e1.png)



