# Anomaly_detection

An outlier detection toolkit for based on Interquartile Range (IQR) and Z-scores.

## Data Set Information

The dataset contains **9358** instances of hourly averaged responses from an array of **5 metal oxide chemical** sensors embedded in an **Air Quality Chemical Multisensor Device**. The device was located on the field in a significantly polluted area, at road level,within an Italian city. Data were recorded from **March 2004 to February 2005** (one year)representing the longest freely available recordings of on field deployed air quality chemical sensor devices responses. Ground Truth hourly averaged concentrations for CO, Non Metanic Hydrocarbons, Benzene, Total Nitrogen Oxides (NOx) and Nitrogen Dioxide (NO2) and were provided by a co-located reference certified analyzer. Evidences of cross-sensitivities as well as both concept and sensor drifts are present as described in De Vito et al., Sens. And Act. B, Vol. 129,2,2008 (citation required) eventually affecting sensors concentration estimation capabilities. **Missing values are tagged with -200 value.** <br>
Source: https://archive.ics.uci.edu/ml/datasets/Air+Quality

## Attribute Information

0- **Date** (DD/MM/YYYY) <br>
1- **Time** (HH.MM.SS)<br>
2- True hourly averaged concentration **CO in mg/m^3** (reference analyzer)<br>
3- **PT08.S1** (tin oxide) hourly averaged sensor response (nominally CO targeted)
4- True hourly averaged overall **Non Metanic HydroCarbons concentration in microg/m^3** (reference analyzer)<br>
5- True hourly averaged** Benzene concentration in microg/m^3** (reference analyzer)<br>
6- **PT08.S2** (titania) hourly averaged sensor response (nominally NMHC targeted)<br>
7- True hourly averaged **NOx concentration in ppb** (reference analyzer)<br>
8- **PT08.S3** (tungsten oxide) hourly averaged sensor response (nominally NOx targeted)<br>
9- True hourly averaged **NO2 concentration in microg/m^3** (reference analyzer)<br>
10- **PT08.S4**(tungsten oxide) hourly averaged sensor response (nominally NO2 targeted)<br>
11- **PT08.S5** (indium oxide) hourly averaged sensor response (nominally O3 targeted)<br>
12- **Temperature** in °C<br>
13- **Relative Humidity** (%)<br>
14- **AH** Absolute Humidity<br>

## Outlier detection
Two methods are provided, whether to compute a statistic on the whole timeseries (i.e. static method) or to compute a statistic on a defined window (i.e. dynamic method)
 **A static method :**

![image](https://user-images.githubusercontent.com/38179853/125199276-5d4b8b80-e25d-11eb-8dae-b0b2e0439874.png)

**A dynamic method :**
![image](https://user-images.githubusercontent.com/38179853/125199304-84a25880-e25d-11eb-9b56-55a6df920bd5.png)
