# Readme

In this paper, we explore a neutral comparison of different methods to recognize attacks on IEC 60870-5-104 based SCADA environments. To achieve that, several machine learning models were created with Matlab and their performance was evaluated by using confusion matrices. These models were trained by a data set created in a test bed of the distribution system operator in Austria. The test bed consisted of several RTUs, switches, a SCADA system and a micro controller to capture network traffic data. The captured data includes  two common reconnaissance attacks, a DoS attack and SCADA specific reconnaissance by the use of an IEC 60870-5-104 protocol fuzzer. To create the data set, Wireshark as well as a Powershell script was utilized to gather the data and convert the Packet Description Markup Language (PDML) format of Wireshark to Comma-Separated Values (CSV) format.


This repository includes the Snort rule set used in the Energy Informatics paper with the title "Comparison of Approaches for Intrusion Detection in Substations using the IEC60870-5-104 Protocol".
