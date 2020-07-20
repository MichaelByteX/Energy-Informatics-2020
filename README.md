# Comparison of Approaches for Intrusion Detection in Substations using the IEC 60870-5-104 Protocol

Here are all data and materials of the following publication made publicly available for further research:

> **Comparison of Approaches for Intrusion Detection in Substations <br>
> using the IEC 60870-5-104 Protocol** <br>
> Michael Egger, Günther Eibl and Dominik Engel <br>
> Energy Informatics (ENINF), 2020

In this paper, we explore a neutral comparison of different methods to recognize attacks on IEC 60870-5-104 based SCADA environments. To achieve that, several machine learning models were created with Matlab and their performance was evaluated by using confusion matrices. These models were trained by a data set created in a test bed of the distribution system operator in Austria. The test bed consisted of several RTUs, switches, a SCADA system and a micro controller to capture network traffic data. The captured data included  two common reconnaissance attacks, a DoS attack and SCADA specific reconnaissance by the use of an IEC 60870-5-104 protocol fuzzer. To create the dataset, Wireshark was utilized to gather the data and convert the Packet Description Markup Language (PDML) format of Wireshark to Comma-Separated Values (CSV) format.

# Usage

## Snort Ruleset
This repository includes the local.rules as well as the protocol-scada.rules file used to evaluate the results in the presented paper with Snort.
In order to use the rules, they have to be copied to the etc/snort folder. 
