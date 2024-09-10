# SmartMeterReader Assignment

## Task description
Your task is to create production-ready software called SmartMeterReader for reading the last hour of data from smart meters. 

SmartMeterReader accepts a command to immediately read measured data from smart meters which store it in a database. 
The command for SmartMeterReader is a HTTPS POST request with JSON body. The JSON contains a list of IP addresses of smart meters for communication. The command example can be found in [read.request.smartmeter-reader.json](./read.request.smartmeter-reader.json).
SmartMeterReader reads the measured data from smart meters via HTTPS GET <smart-meter-ip-address>/read. A response from smart meters is also in JSON format and contains information about measured voltage and amperage at a given time. The example of a smart meter response can be found in [read.response.smartmeter.json](./read.response.smartmeter.json). 

Smart meters always return measured data for every quarter of the last hour. For example, if it is 1:23 AM then returned measured data will be from 00:30, 00:45, 1:00, 1:15. Timestamps are always in ISO 8601. Measured data is in volts and amperes.

SmartMeterReader persists data in a database for future computations.

### Additional information
Any assumptions about behaviour of the SmartMeterReader or the smart meters based on missing information in the task description write to a readme of your application.

The task should take a few hours. Therefore, it is expected that you will:

1. create a skeleton of the application in form of classes and methods with empty bodies but with javadoc or inline comments describing what needs to be done to make it production-ready,
2. choose a single part of the application and write production-ready code.

Use programming language, libraries and other software you are used to working with.

When finished push the code to your public git account which will enable us to clone the project and send the link to tomas.buchta@mycroftmind.com
