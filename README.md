# Simulating Air Traffic With Azure #

---

## Overview ##

This repo was originally content for the Cloud City IoT Hack, an event with a hands-on introduction using some of the best features Microsoft Azure has to offer, including [IoT Hubs](https://azure.microsoft.com/services/iot-hub/), [Event Hubs](https://azure.microsoft.com/services/event-hubs/), [Azure Functions](https://azure.microsoft.com/services/functions/), [Stream Analytics](https://azure.microsoft.com/services/stream-analytics/), and [Cognitive Services](https://azure.microsoft.com/services/cognitive-services/). The four hands-on "labs" are located in folders named HOL 1, HOL 2, HOL 3, and HOL 4. Here's a quick summary of those labs:

- [HOL 1](HOL%201/HOL%201%20-%20MXChip.md) - Creating the Azure IoT Hub and programming the [MXCHIP]([MXChip](https://microsoft.github.io/azure-iot-developer-kit/)) to send accelerometer data.
- [HOL 2](HOL%202/HOL%202%20-%20Functions%20and%20Event%20Hubs.md) - Creating an Azure Event Hub and deploying an Azure Function that transforms the accelerometer data to the IoT Hub into "flight data". This displays the disposition on an airplane, transmiting it to the original Event Hub. Then connectting a UWP client app to the Event Hub and using the gyroscope on the MXChip to fly a simulated airplane.
- [HOL 3](HOL%203/HOL%203%20-%20Stream%20Analytics.md) - Creating a pair of Event Hubs and deploying a Stream Analytics job that analyzes all the air traffic in the room (for aircraft that are within two miles of each another). The UWP app is meant to show the air traffic.
- [HOL 4](HOL%204/HOL%204%20-%20Putting%20It%20All%20Together.md) - Further modifing the Azure Function deployed in HOL 2, to transmit flight data to the input hub used by Stream Analytics. Then also connecting the client app to the Stream Analytics output, therefore modifying the app to transmit specical warning messages back to the MXChip when the aircraft are within two miles of another.

The repo also has five source-code folders additional to the "labs":

- FlySim -> The VSCode solution containing the client app, used to fly the simulated airplanes.
- FlySimEmbedded -> The code uploaded to the MXChip for programming it to send accelerometer data to an Azure IoT Hub.
- FlySimFunctions -> The source code of Azure Functions to process and send accelerometer data from the created Azure IoT Hub into Azure Event Hub.
- AirTrafficSim -> The VSCode solution containing the air-traffic control (ATC) app that shows all the airplanes in flight and highlights those that are within two miles of each other.
- FlySimTest -> The VSCode solution containing the command-line app for injecting simulated aircraft into AirTrafficSim (refer to above). Used for testing and adding airplanes to the ATC sector.


## Contributions ##

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For more information, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.
