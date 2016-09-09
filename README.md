# cmpe281-project
Project was to build a mobile sensor cloud.

This project has different functional components and need to be deployed on EC2 instances. These instances need to configured in order to run the project.

Following gives description of each component for the working of the project:

1.Data obtained from Air Composition sensors using real data from AIRNow API.

2.The Hubs manage these sensors and fetch the data from the sensors.  

3.Data collector running on an EC2 instance will periodically collect data from the hubs and Load it into the database.

4.MongoDB used for the databases. The database servers will be running on a separate EC2 instance.

5.Metadata DB will store details about the sensors allocated to the user while the MongoDB will store data fetched from the sensor.

6.The Data Access Manager running on a separate EC2 instance will fetch the data requested from the user.

7.Another EC2 instance runs the resource manager that will provision Hubs and sensors for the user.

8.Sensor Resource Manager allocates and manages sensors according to the user’s request.

9.Sensor Data Collector periodically collects data from the sensors and load it into the Database.

10.Sensor Data Repository consists of a Database (DB) that stores the data collected by the Data Collector.

11.Sensor Data Access Manager supports the access of existing sensor data from the database.

12.Mobile hub can track and report sensor status, report, and collect the live sensor data based on predefined schedule.

13.Sensor devices are individual programs that fetch data from the sensors periodically.

14.Hubs are components programs allocated on a per user basis which manage collection of data from the sensors provisioned for the users. These hubs can run on separate ec2 instances to support 
scalability as the number of users increases.

15.Data Loaders can also run on multiple instances in a load balancing configuration to redirect requests to free loaders in case of huge data loads (for large number of users and sensors). 

16 Users can view their provisioned sensors from a console dashboard and also request for new sensors.

17.To manage large number of users, a load balanced configuration can also be used where multiple instances are automatically created for the node.js webserver to distribute the load. 

18.Admin can use the Admin console to monitor the cloud system status, check system health, configure and manage sensors, etc.


Infrastructure Diagram.
![alt tag](https://github.com/aditya-dhende/cmpe281-project/blob/master/Picture1.png)

