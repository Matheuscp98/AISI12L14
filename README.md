# 🔩 AISI 12L14 Dataset 

**DOI:**

---

## 📝 Description
This repository provides a **structured experimental dataset** containing **2,448 surface roughness measurements** obtained during **CNC turning of slender shafts** manufactured from **AISI 12L14 free-cutting steel**.

The dataset was generated using a **nested-based crossed experimental design** combining:

- A **Central Composite Design (CCD)** for controllable machining parameters (inner array);
- A **General Full Factorial Design (GFFD)** for noise factors (outer array);

Organized under a **hierarchical (nested) experimental structure incorporating both fixed and random effects.**.

The CCD includes **17 experimental runs**, which were evaluated under **12 noise scenarios**, with **12 replicate measurements per scenario**, resulting in:

> **17 × 12 × 12 = 2,448 observation-level measurements**

Each record corresponds to a specific combination of:

- Cutting speed (`Vc`)
- Feed rate (`f`)
- Machining depth (`d`)

evaluated under multiple noise conditions defined by:

- Shaft diameter ('ϕ')
- Tool flank wear ('VP')
- Axial measurement position ('P')

With **radial measurement locations and replicates nested within the hierarchy**.

The dataset preserves the full acquisition structure:

> **tool wear → diameter → axial position → radial position → replicate**

This organization enables reanalysis using **crossed, nested, or mixed-effects statistical modelling strategies** without requiring access to the original experimental infrastructure.

The dataset is intended for:

- Statistical analysis  
- Design of Experiments (DOE);
- Robust Parameter Design (RPD);
- Response Surface Methodology (RSM); 
- Mixed-effects modelling;
- Manufacturing process modelling;
- Optimization;
- Machine Learning applications. 

**Note:** The main focus of this repository is on the **dataset**.

---

## 📚 Publications

This repository is associated with the following research work:

-  *Manuscript currently under peer review*

---

## 🛠️ How to Use
1. Clone or download this repository.  
2. Open the `.csv` or `.xlsx` files using **Python (pandas)**, **MATLAB**, **R**, **Microsoft Excel**, or equivalent tools.  
3. Use the datasets as follows:  

   - [**Data 12L14**](data.csv) replicate-level surface roughness measurements  
---

## 📂 Repository Structure

| File / Folder | Description |
|---------------|-------------|
| [**README**](README.md) | Documentation of the dataset and usage guidelines. |
| [**Data 12L14**](data.csv) | Observation-level surface roughness measurements. |
| [**LICENSE**](LICENSE) | Dataset license information. |

---

## 📊 Variables

### 🔹 Controllable Variables (CCD — Inner Array)

| Symbol | Description | Unit | Range |
|--------|-------------|------|-------|
| `Vc` | Cutting speed | m/min | 220.00 – 340.00 |
| `f` | Feed rate | mm/rev | 0.08 – 0.12 |
| `d` | Machining Depth | mm | 0.70 – 1.20 |

---

### 🔹 Noise Factors (GFFD — Outer Array)

| Symbol | Description | Unit | Levels |
|--------|-------------|------|--------|
| `ϕ` | Shaft diameter | mm | 30, 50 |
| `VB` | Tool flank wear | mm | 0.0 (new), 0.30 (worn) |
| `P` | Axial measurement position | – | Chuck, Middle, Live centre |

Radial positions (0°, 90°, 180°, 270°) and replicates are **nested within axial positions**.

---

### 🔹 Output Variables (Measured)

Surface roughness parameters obtained directly from profilometer measurements:

| Symbol | Description | Unit |
|--------|-------------|------|
| `Ra` | Arithmetic mean roughness | μm |
| `Rt` | Total height of roughness profile | μm |
| `Ry` | Maximum peak-to-valley height | μm |
| `Rq` | Root mean square roughness | μm |
| `Sm` | Mean spacing of profile irregularities | μm |

Additional amplitude-based descriptors may also be available depending on the dataset version.

---

## 📄 Metadata
All experimental variables and hierarchical relationships are documented in **Metadata.csv**, including:

- Variable names and abbreviations  
- Units  
- Experimental role (input, noise, output)  
- Hierarchical embedding  

This metadata enables complete dataset reuse without access to the original CNC setup.

---

## 📌 Notes on Data Organization

- The dataset is provided exclusively at the **observation level**.
- No pre-aggregated results are included.
- The hierarchical structure supports **nested and mixed-effects modelling**.
- All values correspond to **direct profilometer outputs**.

---

## 🏭 Experimental Context

Machining experiments were performed on a **CNC lathe** using:

- AISI 12L14 slender shafts
- Cemented carbide cutting tool (ISO class P35)
- Contact profilometer measurements

The experiments were conducted under controlled laboratory conditions to ensure repeatability and measurement reliability.

## License
This dataset is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0).  
See the [LICENSE](LICENSE) file for details.

---

## 📬 Contact

<a href="mailto:matheusc_pereira@hotmail.com">
  <img src="https://i.ibb.co/k6Ddn36k/email.png" alt="E-mail" height="60"/>
</a>
<a href="https://www.linkedin.com/in/matheuscostapereira/">
  <img src="https://i.ibb.co/Kx4rZxdr/linkedin.png" alt="LinkedIn" height="60"/>
</a>
<a href="https://scholar.google.com.br/citations?user=1iDBIzYAAAAJ&hl=en-us">
  <img src="https://i.ibb.co/SwsRKK1t/scholar.png" alt="Google Scholar" height="60"/>
</a>
<a href="https://lattes.cnpq.br/7025666927284220">
  <img src="https://i.ibb.co/1fMjS38j/lattes.png" alt="Lattes" height="60"/>
</a>

---

> _Feel free to open issues or PRs, or reach out for collaboration or questions!_

---

## 📜 License
This dataset is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0).  
See the [LICENSE](LICENSE) file for details.
