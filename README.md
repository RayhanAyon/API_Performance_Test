# API Performance Test
## Description:
I tested how Booking APIs handle heavy traffic (Load and Stress Testing). Then, I connected multiple API requests (API Chaining) for DMoney’s Transaction APIs using JMeter. 
I used data from CSV files and ran multiple API requests at the same time with four threads in JMeter.

## Test scenario for Load and Stress Test
1. Create a collection of Login API, Create Booking API and Search API in Jmeter.
2. Perform load and stress test to find the Actual TPS and Bottleneck Point.
- Used a Gaussian Random Timer (Deviation 2000ms, Constant delay 500ms). Do it in 3 step
  - 1st step: 5 min load
  - 2nd step: 10 min load
  - 3rd step: 20 min load
- API:-  https://restful-booker.herokuapp.com

## Test scenario for Dmoney API Flow
1. Log in as an admin once.
2. 5 agents perform deposits for 10 customers.
3. 5 customers send money to another 10 customers.
4. 5 customers make payments to 2 merchants.
- Set the ramp-up time to 120 seconds in all the above thread configurations.
- Website for APIs - http://dmoney.roadtocareer.net

## Technology I Used
- Jmeter

## How To Run?

### Execute the following steps using JMeter (GUI Mode)
- Clone this project.
- Open ApacheJMeter.
- From ApacheJMeter open the JMX File.
- Run.

### Execute the following steps using CLI Mode
- Clone this project.
- ```jmeter -n -t booking.jmx -l booking.jtl -e -o Report``` [For Booking API]
- ```jmeter -n -t .\Dmoney.jmx -l .\Dmoney.jtl -e -o Report``` [For Dmoney Transaction API]
## Load and Stress Test Excel Repoet
https://docs.google.com/spreadsheets/d/1Dzn9rHw2GyMEA8bA__NlPu_Y1dxZIj8jxD3LprRlv0Y/edit?usp=sharing

## HTML report for Load Test
![image](https://github.com/user-attachments/assets/19a3a9e7-c77d-4b4d-9de1-bcdf55c79e29)

## HTML report for Stress Test
![image](https://github.com/user-attachments/assets/e9d12037-72a6-45b0-822d-09af64be4de6)

## HTML report for DMoney Jmeter Collection Test
![image](https://github.com/user-attachments/assets/f2e13938-bd83-4ed2-98d4-f76aeac4a44b)

