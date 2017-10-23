# Azure IoT Hub with routes and endpoints
Sample Azure IoT provisioning with routes to cold storage, Time Series Insights and Event Hubs

## How to
This sample leverages PowerShell for deploying to Azure using Azure Resource Manager templates. ARM templates can be used in Azure CLI if you prefer. Below how you can use the powershell scripts.

1. Make sure you have the Azure Tools installed (Powershell)
2. Clone this repo
3. Log into Azure `Login-AzureRm`
4. Sample in folder `/deploy/iot-routes-tsi`: creates IoT Hub with 3 routes, 2 endpoints; Event Hubs, Time Series Insights and a Storage account. The default messages/events endpoint is set as a route. All routes have empty conditions, it is recommended you use your own conditions to route specific messages to the different endpoints. But as a sample it's left to route all messages.
5. Run the script `.\01-provision.ps1` and pass the parameters as required.
Example: ` .\01-provision.ps1 -SubscriptionName [yoursubname] -DeploymentPrefix [uniqueprefix] -Location "West Europe"`
6. It takes about 5 minutes to provision the resources.


Provided as sample - 'AS IS'





