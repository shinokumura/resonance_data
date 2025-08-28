# Experimental Resonance Parameter Data from EXFOR

This repository contains (and will continue to contain) resonance parameters, resonance spacing (D0, D1), resonance integrals, level densities, and strength function datasets extracted from the [EXFOR Master Files](https://github.com/IAEA-NDS/exfor_master) using the [EXFOR Parser](https://github.com/IAEA-NDS/exforparser).  

## General Information  
The data in this repository is currently under testing and is subject to change. The repository will be updated irregularly based on updates to the [EXFOR Master Files](https://github.com/IAEA-NDS/exfor_master) and the [EXFOR Parser](https://github.com/IAEA-NDS/exforparser).  

### **EXFOR Data Table Columns:**  
- **EXFOR ID**: EXFOR entry number (5 digits) – subentry number (3 digits) – pointer number (1 digit), e.g., `12345-002-0`.  
- **First author**: Name of the first author.  
- **Year**: Year of publication.  
- **en_inc**: Incident neutron energy in MeV.  
- **den_inc**: Uncertainty of the incident neutron energy in MeV.  
- **data**: Cross-section in barns or eV (for gamma_gamma and resonance spacing).  
- **ddata**: Uncertainty of the cross-section in barns or eV (for gamma_gamma and resonance spacing).  
- **sf8**: Reaction modifiers. See details under `Modifiers` in [EXFOR dictionary - diction:34](https://github.com/IAEA-NDS/exfor_dictionary/blob/accc6196f0b1c648c8bf39ef15156c6e7599a920/src/exfor_dictionary/latest.json#L20070C24-L20070C48).  
- **sf9**: Data type. See details under `data types` in [EXFOR dictionary - diction:35](https://github.com/IAEA-NDS/exfor_dictionary/blob/main/src/exfor_dictionary/latest.json#L20422).  
- **Momentum L**: Angular momentum (L) of the resonance when specified.  
- **SPIN J**: Spin (J) when specified.  
- **PARITY**: Parity of the resonance when specified.  

---

## Download All Files  
### **By Git Command**  
Clone the repository from a terminal using:  
```sh
git clone https://github.com/shinokumura/resonance_data.git
```

### **Download as Zip File**  
Download from [this link](https://github.com/shinokumura/resonance_data/archive/refs/heads/main.zip).  

---

## 📁 **Data Examples**  

### **1. Resonance Integral**  
Example: [(25-MN-55(N,G),,RI)](https://github.com/shinokumura/parameters_data/blob/main/resonance_integral/n-g/25-MN-55.txt)  

- **EXFOR Entry #20314002**  
   - [EXFOR Master File](https://github.com/IAEA-NDS/exfor_master/blob/main/exforall/203/20314.x4)  
   - [EXFOR Data Explorer](https://nds.iaea.org/dataexplorer/exfor/entry/20314-002-0)  

---

### **2. MACS (Maxwellian-Averaged Cross Section)**  
Example: [(57-LA-139(N,G),,SIG) at ~30 keV](https://github.com/shinokumura/parameters_data/blob/main/macs/n-g/57-LA-139.txt)  

- **EXFOR Entry #23042002**  
   - [EXFOR Master File](https://github.com/IAEA-NDS/exfor_master/blob/main/exforall/230/23042.x4)  
   - [EXFOR Data Explorer](https://nds.iaea.org/dataexplorer/exfor/entry/23042-002-0)  

---

### **3. Gamma_gamma (Averaged Capture Width)**  
Example: [(73-TA-181(N,G),,WID,,AV)](https://github.com/shinokumura/resonance_data/blob/main/gamma_gamma/n-g/73-TA-181.txt)  

- **EXFOR Entry #10577040**  
   - [EXFOR Master File](https://github.com/IAEA-NDS/exfor_master/blob/main/exforall/105/10577.x4)  
   - [EXFOR Data Explorer](https://nds.iaea.org/dataexplorer/exfor/entry/10577-040-3)  

---

### **4. Resonance Spacing**  
Example: [(94-PU-239(N,0),,D)](https://github.com/shinokumura/parameters_data/blob/main/resonance_spacing/n-0/94-PU-239.txt)  

- **EXFOR Entry #40104007**  
   - [EXFOR Master File](https://github.com/IAEA-NDS/exfor_master/blob/main/exforall/401/40104.x4)  
   - [EXFOR Data Explorer](https://nds.iaea.org/dataexplorer/exfor/entry/40104-007-0)  


### **4. Resonance Parameters**  

#### *1. Single-Level Resonance Widths (&#915;)*

REACTION Coding:
- (…(N,TOT),,WID) = total width (&#915;)
- (…(N,G),,WID) = capture width (&#915;_&#947;)
- (…(N,F),,WID) = fission width (&#915;_F)

Resonance Energy Coding:
- (...(N,0),,EN) = Determined by the author
- In the data table using the heading `EN-RES` = The resonance energy not assigned by the author

Unit: eV

Example: [(92-U-235)](https://github.com/shinokumura/resonance_data/blob/main/resonance_parameter/N/U-235/WID/92-U-235_A.Michaudon-20727-006_1965.txt)  

- **EXFOR Entry #20727006**  
   - [EXFOR Master File](https://github.com/IAEA-NDS/exfor_master/blob/5e570ba94b33a14ce7180935d060bfa4dd879035/exforall/207/20727.x4#L11097)  
   - [EXFOR Data Explorer](https://nds.iaea.org/dataexplorer/exfor/entry/20727-006-3)  


#### *2. Reduced neutron widths*
REACTION coding:

- (…(N,EL),,WID/RED)

Unit: eV

Example: [(92-U-235)](https://github.com/shinokumura/resonance_data/blob/main/resonance_parameter/N/U-235/WID-RED/92-U-235_O.D.Simpson-12412-002_1956.txt) 

- **EXFOR Entry #12412002**  
   - [EXFOR Master File](https://github.com/IAEA-NDS/exfor_master/blob/5e570ba94b33a14ce7180935d060bfa4dd879035/exforall/124/12412.x4#L20C1-L20C13)  
   - [EXFOR Data Explorer](https://nds.iaea.org/dataexplorer/exfor/entry/12412-002-1)  



#### *3. Reduced Area (Scattering Area)*
REACTION coding:

- (…(N,EL),,ARE)

Unit: B*E

Example: [(92-U-235)](https://github.com/shinokumura/resonance_data/blob/main/resonance_parameter/N/U-238/ARE/92-U-238_F.C.Difilippo-10694-003_1980.txt) 







---

## ✅ **Notes**  
- The data structure and formatting follow the YANDF format.  
- This repository is intended for research and reference purposes and will be integrated into the [IAEA Nuclear Reaction Data Explorer](https://nds.iaea.org/dataexplorer/).  
