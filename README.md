# Project Title
**IIOT system for Total Quality Maintenance**

## Getting Started
* Clone the repo
* Install prerequiste packages
* Create a FavorIOT package
* Open the CapIOT.Ivproj

## Prerequisites
* Labview 2017+
* Labview TCP/IP modbus package
* Labview .NET package
* Labview HTTP Rest Package
* FavorIOT account
* IMPULSE WINDING TESTER VE2882A4-5U
* DELTA PLC DVP-12SE
* Stator Coil

## Description
The main objective of this project titled “Accumulation and analysation of IIOT data using LabVIEW VIs” is to implement IOT system for Impulse Winding Tester machine and analyse the TPM variable from the data. The six big losses that occurs in the production decreases the productivity and hence the profits of company by a significant margin. The main aim of my project is to reduce the downtime and inactivity by implementing the TPM analysis technique in real time with additional modules for streamlining the production and quality check process. In this project the 3 phase and 5 phase Stator coil is used for comparative analysis with the pre assigned value of the correct Stator coil. The machine used for this operation is called Impulse Winding Tester which compares and measures the impedance and D-Area of the coil. It runs on constant current mode on all phases and measures the other parameters accordingly.
By implementing the IIOT framework, I divided the project into multiple sub module performing together for a smoother and easily modifiable system. To reduce the downtime and inactivity, a SMTP module for shift start and inactivity notification was added. The .Net Framework in LabVIEW was used to perform this operation. The HTTP REST package on Labview gave the feature to send data on a free Cloud platform called FavorIOT to store data log. Accumlation of data was handled by installing Delta PLC to the Impulse Winding Tester. The 4096 and 4098 holding register of Delta PLC was read using the Modbus module in LabVIEW. A GUI dashboard was developed to show real time activity graph, Pass/Fail/Total count. It also showed the TPM parameters such as OEE, Availability, Performance and Quality. To reset all these operations after every 8hr shift, a reset sub module was developed to provide batch wise operation on data. Moreover, for additional security a password authentication submodule was created internally in LabVIEW.
All these submodule working together incorporated the major building block of an IOT system:
* Data Acquisition
* Data Monitoring
* Data Analysis
* Data Logging

## Working
1. A delta PLC was configured to read data from Impulse Winding tester
2. Impulse Winding tester compared the impedance and D-area with the correct stator coil
3. The Fail and Pass count are stored in the holding register of Delta PLC
4. The holding register is read from the Ethernet Modbus module of LabVIEW
5. Data is processed on LabVIEW
6. Downtime, OEE, Pass/Fail/ Availability, Performance and Quality is measured
7. A custom GUI dashboard is made on LabVIEW SubVI
8. A reset block after every 8hrs is created
9. Every 8hr shift data is stored in a csv file
10. A continuous session data is stored on FavorIOT cloud
11. A login system with password protect was installed
12. SMTP notification were send if any malfunction happened

## Results
<p align="center">
  <img src="https://github.com/RishabhSisodia/IIOT-system-for-Total-Quality-Maintenance/blob/master/Output.JPG" alt="Project Layout" width="600px" height="300px"/>
</p>


## Contributors

Created the project as a Capstone project undertaken at Varroc Group.


## License

This project is licensed under the MIT License - see the [LICENSE.md](https://github.com/RishabhSisodia/Virtual-Reality-Arm-Gear/blob/master/LICENSE) file for details
