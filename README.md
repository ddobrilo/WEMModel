# WEMModel
Model for Working Environment Monitoring in Smart Manufacturing

The WEMModel is developed as a proposal of the model for working environment monitoring in smart manufacturing system based on wireless sensor technologies and MQTT protocol and the design of a testing platform. 

## Simulation of WEMModel performance with the testing platform

The testing platform can be used for model validation, prototype application development, and student teaching in engineering education process.

The testing platform is designed as follows:
1.	Sensor nodes are based on Arduino/Genuino UNO Rev3 clones with integrated ESP8266 module. Total of 10 sensor nodes is developed and used in scenarios. The sensor nodes are presented in Figure 6 and have the following configuration: 
-	Wemos D1 R2 – 5 pcs. (four with MQ-135 and one with MQ-2 sensor),
-	Espduino – 2 pcs. (one with MQ-135 and one with MQ-2 sensor), and
-	NodeMCU 12E v1.0 – 3 pcs. (all three with MQ-135 sensor).
2.	Laptop as a system hosting computer with the following components: CPU Intel(R) Core(TM) i3-4005U CPU @ 1.70GHz, 4 GB RAM, DDR3 450 GD SATA HDD, internal WLAN adapter (optionally with TP-Link 722N external USB WLAN adapter), and
3.	Wireless Access Point / router

Software components of the system are: 
1.	Windows 10, Mosquitto broker, Python script for subscription (irrelevant for the testing), screen display and write to SQLite database (irrelevant for the testing), in-stalled on the laptop described above.
2.	Wireshark Network Analyzer tool installed on the sam laptop.

![Figure1](images/WEMFigure_07.png)
Figure: Deployment and connectivity of testing platform components

The platfrom is tested with 4 scenarios

1.	4 sensor nodes, data send interval: 5 sec - 0.62 pckts./sec server load
2.	4 sensor nodes, data send interval: 200 msec - 11.82 pckts./sec server load
3.	4 sensor nodes, data send interval: no delay - 51.10 pckts./sec server load
	- WEMModel_3rd.Scenario.zip - zipped Wireshark pcapng file and exported CSV data for analyses (available for download)
4.	10 sensor nodes, data send interval: no delay - 174.11 pckts./sec server load
    - WEMModel_4th.Scenario.zip - zipped Wireshark pcapng file and exported CSV data for analyses (available for download)

## Simulation of Data Analyses module

The example of Data Analyses module is presented her. This module assumes the usage of sensor nodes with integrated dust sensor. Analysis of the data collected by the sensors was done on data related to dust particle distribution and numerous harmful gases, so in the real system it is a mixture of harmful substances. Of course, dust is not the only type of pollution, but the presence of dust is one of the key parameters of the environment considered here. Bearing in mind that we were not able to deploy and use the sensors in a real environment for a long time, we used a simulation, with the aim of proving the validity of the concept.

The 'train.7z' file contains the images used for the Convolutional Neural Network (CNN) training. Images are classified into four classes (folders): 'both', 'none', 'top-left' and 'bottom-right'. The 'test.7z' file contains the images used to test the trained CNN.

The images are 100 by 50 pixels, 75 dpi, and were created using bilinear interpolation
![Figure2](images/WEMFigure_03.jpg)
Figure: Deployment of sensors in simulation

I you use this data for the research please cite it as:

Dalibor Dobrilovic, Vladimir Brtka, Zeljko Stojanov, Goran Jausevac, Dragan Perakovic, and Gordana Jotanovic, 2021, WEMModel dataset, https://github.com/ddobrilo/WEMModel
