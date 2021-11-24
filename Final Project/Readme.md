# Design a Highly Avaiable Web application


### Architechture overview

![image](https://user-images.githubusercontent.com/91851332/143194293-1c91e231-9a55-4f61-9532-1a7fcf4fcca1.png)

# VPC

### 1. Creating a VPC - ( 10.0.0.0/16)

![image](https://user-images.githubusercontent.com/91851332/143185212-3415fbea-81f5-4b3e-9a86-dbd9de06282e.png)


### 2. Creating 4 subnets - (10.0.0.0/24)

![image](https://user-images.githubusercontent.com/91851332/143185453-147eabdb-8945-436b-9b38-a600f97215dd.png)


### 3. Create RouteTable - 1 for Webserver and 1 for Database Server

![image](https://user-images.githubusercontent.com/91851332/143186842-58162c8f-da3b-4ea4-9fc4-75822e90d3d4.png)


### 4. Creating IGW for Outside access and Attaching it to WebServer Route table.

![image](https://user-images.githubusercontent.com/91851332/143187319-1d113d53-3490-48d4-9f53-70c13cb683e1.png)


### Final VPC setup

![image](https://user-images.githubusercontent.com/91851332/143187836-99cbeb32-2f85-4533-ad4b-6b6152419930.png)


# Creating Security Groups

### One For ALB

![image](https://user-images.githubusercontent.com/91851332/143194592-9811d422-2947-4a91-a20d-4a1a18a929a7.png)


### One for EC2

![image](https://user-images.githubusercontent.com/91851332/143195067-97710e61-4a3b-43c4-be06-df411c31b1b0.png)


# Creating ALB and ASG

### Creating Target Group -> Create a Application load balancer


![image](https://user-images.githubusercontent.com/91851332/143190553-f1be7657-1736-4930-af1e-46fbad02015c.png)


### Creating a Launch Template for ASG and Creating an ASG + mapping it to loadbalancer

![image](https://user-images.githubusercontent.com/91851332/143191635-b0f25c06-f351-49ed-993c-04ac37467b01.png)


### After Creation of ASG, it launches instances inside the target groups

![image](https://user-images.githubusercontent.com/91851332/143192639-2da2087b-2f58-4414-a308-441df1da2286.png)

### Final Architechtire with ASG and ELB

![image](https://user-images.githubusercontent.com/91851332/143193457-a0081852-6c35-46c6-bb2b-4a5eb9b14abe.png)

# Integrating with Route53

![image](https://user-images.githubusercontent.com/91851332/143194272-31dfd2d0-2eea-4781-a3cd-dddcbad76b90.png)






