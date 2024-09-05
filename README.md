# From Clicks to Deliveries <br>

<h4>Description : </h4>
As an e-commerce company, our success hinges on seamlessly integrating our online platform with efficient logistics management to ensure optimal customer satisfaction and operational efficiency. To achieve this synergy, we aim to leverage real-time data streams from both our website and fleet of delivery trucks. <br><br>

<h4>Tools used : </h4>
<li>Python</li>
<li>Boto3</li>
<li>API Gateway</li>
<li>AWS Kinesis</li>
<li>AWS Lambda Function</li>
<li>AWS DynamoDB</li>

<h4>Online Platform Optimization : </h4>
We need to analyze clickstream data to understand customer preferences, enhance user experience, and optimize marketing strategies for key product categories such as mobile phones, laptops, and cameras.<br>

For 3 items following data is collecting in real time : <br>
<li>Item ID</li>
<li>Item Name</li>
<li>Click Count</li>
<b>[All data used here are random and simulated using the Python file click_producer.py]</b><br><br>

<h4>Fleet Management and Logistics Optimization : </h4> 
Simultaneously, we must monitor and analyze real-time telemetry data from our fleet of delivery trucks, utilizing IoT sensors installed in each vehicle. This data will enable us to optimize routes, reduce fuel consumption, proactively address maintenance issues, and ensure the safety and reliability of our delivery operations. <br><br>

For 3 truck in the fleet, the following data will be collected in near real-time(the trucks are sending the data every 1 minute): <br>
<li>Truck ID : should have 3 truck id’s</li>
<li>GPS Location: Latitude, Longitude, Altitude, Speed.</li>
<li>Vehicle Speed: Real-time speed of the vehicle.</li>
<li>Engine Diagnostics: Engine RPM, Fuel Level, Temperature, Oil Pressure, Battery Voltage.</li>
<li>Odometer Reading: Total distance traveled.</li>
<li>Fuel Consumption: Fuel usage over time.</li>
<li>Vehicle Health and Maintenance: Brake status, Tire pressure, Transmission status.</li>
<li>Environmental Conditions: Temperature, Humidity, Atmospheric Pressure.</li>
<b>[All data used here are random and simulated using the Python file click_producer.py]</b><br><br>

<strong>Workflow : </strong><br><br>
>> The Clickstream data is collected in realtime using AWS Kinesis and sent to a Lambda function to process and store the data in DynamoDB
>> The Truck IOT data is collected once every 1 minute, posted to an API which triggers a Lambda function and stores the data in DynamoDB<br><br>

> [!CAUTION]
> <strong>Note : <br>
> Before executing the codes make sure you have the necessary packages installed in your environment<br>
> Make sure you've properly edited and provided your credentials wherever required <br>
> All data used in this project are randomly generated using python files<br>
