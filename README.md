# Algan UAV Teknofest Technology Team GUI Demo

​	The Graphical User Interface(GUI) is designed as well developing for Algan UAV Technology team. This GUI demonstrates telemetry data and live camera view of the UAV with some process. Furthermore, some special image processing of the out of the GUI is carrying out with our AI Competitor UAV Detection model. 

​	Firstly, with the configurated UAV to be connected which is preparing to take-off, the connection with the UAV is provided by the connection tab's settings as it is shown below named "IHA Bağlantı"(UAV Connection). After the successful connection, the instant telemetry data of the UAV will be able to seen in the "TCP Verileri" tab like"Latitude", "Longitude", "Altitude" etc. 

   Moreover in "IHA Goruntu"(UAV Display) tab, the live camera view of the UAV can be seen with some informative text that indicates the current situation of the UAV such as "Mission Mode", "UAV Control" and "GPS Clock". Simply put, there are two modes to perform the tasks given by Teknofest, which are "Locking" and "Kamikaze". The modes can be easily changed by the pilot's control with his transmitter. On the left of "IHA Goruntu"(IHA Display) tab, there are some information that is created during flight. The explanation of what are they for is below under the "Categories of the GUI" tab.

​    To sum up, This UAV GUI is to connect the UAV, to see the telemetry data of the UAV as well displaying the processed live camera view with the model of UAV Detection or another mode's necessarities. As there are more detailed explanation below, you should dive into to read to learn what does the program do especially along the processes in the background. If you are reading this article and be interested in aviation with Teknofest Competition, see you there at Teknofest 2023. 

<p align="center">
    <img src="https://user-images.githubusercontent.com/70758836/216790198-72316eb9-ff11-49c6-ba94-70ff67edc5ea.png"
</img>
</p>

<p align="center"> General Appearence of Algan GUI</p>

# Categories of the GUI 

<p align="center">
    <img src="https://github.com/kadirtuna/AlganGUIDemo/blob/main/Images/AlganGUIDemo2.png?raw=true"
</img>
</p>

### 1 - IHA Baglanti (UAV Connection) Tab:

​	This part is to connect with the UAV which is prepared to take-off. With typing some informations to connect, the connection process is performed on the back-end. With giving the "Ground Station IP", "Main Server IP", "TCP_Port", "UDP_Port" to the ground station's "IHA Baglanti"(IHA Connection) part, a TCP and a UDP sockets are initializing with the UAV. If the connection is succesfully established, "IHA Bağlantı Durumu" (The connection status) label lights on with the green color. Otherwise, it will be filled out with the red background color to warn the GUI User failing to connect.

![IHA_Connection Image](https://github.com/kadirtuna/AlganGUIDemo/blob/main/Images/IHA_Connection.jpg?raw=true)

<p align="center">IHA Baglanti(IHA Connection) Tab Appearence</p>

### 2 - TCP Verileri(TCP Data)

   The data taken using TCP socket connection appears in this tab. Some data of the UAV to be evaluated by pilot or system manager is put on the page for acquiring the crucial data. As the tab shows, the instant data that is sending "Team Number", "Latitude", "Longitude", "Altitude", "Standing Angle", "Orientation Angle", "Bank Angle", "Speed", "Battery Indicator", "Mission Mode" and GPS clock in a row vertically by the UAV.

<img align="center" src="https://github.com/kadirtuna/AlganGUIDemo/blob/main/Images/Telemetry_TCP_data.jpg?raw=true"></img>

<p align="center">TCP Verileri(TCP Telemetry Data) Tab Appearence</p>

### 3 - IHA Görüntü(IHA Display)

​	As seen there, the live camera view is sending to the GUI by the UAV. However, All frames is processing frame by frame with our AI Model to perform some tasks. Though you see the display tab with the "Locking Mode", there are two modes named "Locking Mode" and "Kamikaze Mode" actually. If our team wants to try to lock any UAV in the air, the pilot will switch on this mode with its transmitter. Then our model which detects any UAV in the frame provides the location of the competitor UAV to our ground station's back-end. Afterwards, our complex python scripts equipped with a lot of algorithms give directions to the UAV from the ground station using UDP socket connection. Therefore the UAV is directed to make an orientation, detection and locking by the ground station. 

   The second one is "Kamikaze Mode" to read the QR code which is planned to be seen of the camera in front of the UAV. The display shows a bounding box that is limited by Teknofest Rules. If our camera would detect any qr code in the boundaries of the box, the "Read QR Code" is going to be seen in the GUI. Therefore the mission is going to be successfull and our system will send the qr code data to the Teknofest's Server(Named Main Server before).

​	During these both modes, "GPS Clock", "Mission Mode", "IHA Control" data and "The Read QR Code" as well "IsLocked", "Locking Time" and "The Best Locking Time" data can be seen in the frame depends on the mission.

![IHA_Display_Image](https://github.com/kadirtuna/AlganGUIDemo/blob/main/Images/IHA_Display.jpg?raw=true)

<p align="center">IHA Goruntu(IHA Display) Tab Appearence</p>

​    All of these progress is happening on the back-end of the program developed with long process by me and my colleouges. Hopefully, Algan UAV Technology team is going to have the best across its straggling and hard work.



# Authors

- [@kadirtuna](https://github.com/kadirtuna)



# Contacts

- [Algan UAV Team - LinkedIn](https://www.linkedin.com/company/algan-uav/mycompany/)



