# Comparison of Approaches for Intrusion Detection in Substations using the IEC 60870-5-104 Protocol

Description of the data used in the paper "Comparison of Approaches for IntrusionDetection in Substations using the IEC60870-5-104 Protocol"
written by Michael Egger, Günther Eibl and Dominik Engel
The paper is already accepted and will be presented at the energy informatics conference 2020 and published in the journal "Energy Informatics"

Data can be used freely for research purposes, if you cite the paper:

> **Comparison of Approaches for Intrusion Detection in Substations <br>
> using the IEC 60870-5-104 Protocol** <br>
> Michael Egger, Günther Eibl and Dominik Engel <br>
> Energy Informatics (ENINF), 2020

In this paper, we explore a neutral comparison of different methods to recognize attacks on IEC 60870-5-104 based SCADA environments. To achieve that, several machine learning models were created with Matlab and their performance was evaluated by using confusion matrices. These models were trained by a data set created in a test bed of the distribution system operator in Austria. The test bed consisted of several RTUs, switches, a SCADA system and a micro controller to capture network traffic data. The captured data included  two common reconnaissance attacks, a DoS attack and SCADA specific reconnaissance by the use of an IEC 60870-5-104 protocol fuzzer. To create the dataset, Wireshark was utilized to gather the data and convert the Packet Description Markup Language (PDML) format of Wireshark to Comma-Separated Values (CSV) format.

# Usage

## Snort Ruleset
This repository includes the local.rules as well as the protocol-scada.rules file used to evaluate the results in the presented paper with Snort.
In order to use the rules, they have to be copied to the etc/snort folder of your Snort installation.

## Dataset
The datasets are saved as csv-files with a ; as a delimiter between columns and are divided into 2 parts

1.) Original data that you need, if you want to create your own features
- csvDataOrigNormal.csv contains the original measurements of normal data
The column names are described in the paper on pages 7 and 8
Missing data are coded as NaN.
- csvDataOrigAttacks.csv contains the original measurements of all the attack data
In order to distinguish the attacks, the last column (called attack) contains the attack type coded as follows
1	SynFlood
2	Portscan Nmap
3   Vulnerabilityscan Nessus
4	Fuzzytest Fuzzy

2.) Data consisting of the features that we created. You might prefer to use these data, if you want to test some new algorithms
These data are divided into a training set and a test set.
Division into training and test is done for usage in a semi-supervised setting: so training data only contain normal packets (attack =0), test data contain all kinds of attacks coded as above and also normal traffic.
Usage for unsupervised setting: put it all together.
Usage for supervised: regroup it as you need it.

"Well, that's it and keep on dancing" [1]
Günther Eibl

[1] Bingo Boys "How To Dance",  Billboard-Hot-100-Charts, begin of 90s
