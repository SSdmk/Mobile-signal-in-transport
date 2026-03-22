# Mobile Signal in Transport Vehicles Dataset

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

Welcome to the **Mobile Signal in Transport** open database. This repository contains extensive measurement data of mobile network coverage (LTE/5G) and GNSS accuracy, collected primarily inside various transport vehicles (such as railway carriages). 

This dataset was created as part of a Bachelor's thesis at **[Názov tvojej univerzity, napr. Brno University of Technology]**.

## 📌 About the Project
The main objective of this research is to evaluate the performance of mobile networks in dynamic transport environments. The project covers:
* Comparison of different measurement hardware (smartphones, modems, wireless development kits) in both real-world conditions and an anechoic (shielded) chamber.
* Evaluation of how the placement of measurement equipment inside a vehicle affects signal quality and GNSS precision.
* Extensive measurement campaigns focused on railway network coverage.

## 📂 Repository Structure
To keep the data organized and accessible, this repository is structured as follows:

* `/data/raw/` - Original, unprocessed logs exported directly from the measurement devices.
* `/data/processed/` - Cleaned, aggregated, and structured `.csv` files ready for data analysis and visualization.
* `/data/data_dictionary.md` - Detailed metadata explaining every column, unit, and variable found in the datasets.
* `/docs/` - Supplementary documentation, including photos of hardware setups and specific device placements inside the vehicles.

## 📡 Hardware & Methodology
Measurements were conducted using a variety of devices to ensure a comprehensive hardware comparison. Devices used include:
* **Smartphones:** [Napr. Samsung Galaxy S23 Ultra]
* **Modems:** [Napr. Quectel RM500Q-GL]
* **Dev Kits:** [Napr. u-blox EVK]

**Measurement Methodology:** Data was collected under various conditions, testing different device placements (e.g., near windows, on tables, inside bags) to measure signal attenuation caused by the vehicle's body (e.g., metalized windows in modern trains). 

## 🚀 How to Use the Data
All processed data is provided in standard, open `.csv` format to ensure compatibility with Python (Pandas), R, MATLAB, or standard GIS software. 

For a complete explanation of the variables (like RSRP, RSRQ, SNR, or GNSS coordinates), please read the `data_dictionary.md` located in the `/data` folder.

## ✍️ Author & Contact
* **[Tvoje Meno a Priezvisko]** - *Bachelor student* - [Odkaz na tvoj LinkedIn alebo e-mail]
* **Supervisor:** [Meno a titul tvojho školiteľa]
* **Institution:** [Názov fakulty a univerzity]

## 📄 License
This dataset is published under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. You are free to use, share, and adapt the data for academic or commercial purposes, provided you give appropriate credit to the original author.
