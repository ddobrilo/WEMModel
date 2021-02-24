# WEMModel
Model for Working Environment Monitoring in Smart Manufacturing

The WEMModel is developed as a proposal of the model for working environment monitoring in smart manufacturing system based on wireless sensor technologies and MQTT protocol and the design of a testing platform. The testing platform can be used for model validation, prototype application development, and student teaching in engineering education process.

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

(ddobrilo/WEMModel/images/WEMFigure_01.png)

