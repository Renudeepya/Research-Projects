# Research Projects

## 🧬 GLUT3 Inhibitor Discovery for Cancer Therapy

### Overview
Computational drug discovery study identifying novel GLUT3 inhibitors for treating glioblastoma, lung cancer, breast cancer, and pancreatic cancer.

### Methodology
- **Virtual Screening**: 85,000 compounds screened using AutoDock Vina
- **QSAR Modeling**: Random Forest algorithm (R² = 0.69)
- **ADMET Profiling**: Drug-likeness and toxicity prediction
- **Molecular Dynamics**: 200 ns simulations using GROMACS
- **Binding Energy**: MM-PBSA calculations

### Results
Five lead compounds identified with strong binding affinity and drug-like properties:

| Compound | Binding Energy | Predicted IC₅₀ | Key Features |
|----------|----------------|----------------|--------------|
| GLUT3-INH-03 | -42.8 kcal/mol | ~50 nM | Benzothiazole scaffold, highest selectivity |
| GLUT3-INH-05 | -37.9 kcal/mol | ~100 nM | Easy synthesis, excellent selectivity |
| GLUT3-INH-02 | -39.4 kcal/mol | ~80 nM | Quinoline core |
| GLUT3-INH-01 | -35.2 kcal/mol | ~150 nM | Piperidine-based |
| GLUT3-INH-04 | -34.8 kcal/mol | ~200 nM | Hydrophobic interactions |

### Key Achievements
- Novel chemical scaffolds with no prior IP conflicts
- High selectivity for GLUT3 over GLUT1 (1.8-4.2 kcal/mol)
- Favorable properties: oral bioavailability, BBB penetration, low toxicity
- Stable binding confirmed through MD simulations

### Tools Used
Python, GROMACS, AutoDock Vina, MODELLER, RDKit, SwissADME, pkCSM

---

## 🌐 Network Protocol Configuration (STP & VLAN)

### Overview
Implementation of Spanning Tree Protocol with VLAN-based load balancing across two branch office networks.

### Network Setup
- **Topology**: 2 branch offices, 4 VPCs, 2 switches with dual trunk links
- **VLANs**: VLAN 10 and VLAN 20 for network segmentation
- **IP Range**: 10.1.1.0/24

### Implementation
1. **VLAN Configuration**: Created VLANs 10 and 20 on both switches
2. **Trunk Links**: Configured 802.1Q encapsulation for redundancy
3. **STP Optimization**: Cost tuning for load balancing
4. **Testing**: Verified connectivity across all endpoints

### Deliverables
- IP addressing schema for all devices
- STP blocking port documentation
- Load balancing configuration
- Full connectivity verification

### Technologies
Cisco IOS, STP, VLANs, 802.1Q Trunking, DHCP

---

<div align="center">

⭐ Star this repository if you find it useful!

</div>
