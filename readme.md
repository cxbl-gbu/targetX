# 🎯 TargetX: Precision Bacterial Drug Target Identification

**TargetX** is an automated bioinformatics pipeline designed to rapidly screen potential drug targets from an extensive bacterial dataset. TargetX uses a systemic "negative-to-positive" filtering strategy to filter thousands of protein sequences to a handful of candidates that are essential far the survival of pathogen.

---

## 🧬 Step-wise Workflow

TargetX doesn't just search; it eliminates. The pipeline moves through a rigorous multi-stage funnel:

1.  **Redundancy Reduction (CD-HIT):** Collapses duplicate or highly similar sequences (90% threshold) to minimize computational overhead.
2.  **Host Safety Filter (Human Proteome):** A negative filter to remove proteins homologous to human sequences, preventing cross-reactivity.
3.  **Essentiality Check (DEG):** A positive filter against the *Database of Essential Genes* to ensure the target is critical for bacterial survival.
4.  **Virulence Assessment (VFDB):** Identifies proteins involved in pathogenesis and toxicity.
5.  **Broad-Spectrum Check (ESKAPE):** Filters against the most notorious multi-drug resistant pathogens.
6.  **Subcellular Localization (PsortB):** Pinpoints the protein's location to determine accessibility for drug molecules.

---

## 🚀 Performance Snapshot
In recent benchmarks, TargetX processed:
* **Input:** 10 *E. coli* Proteomes (~53,223 sequences).
* **CD-HIT Execution:** Reduced to 11,619 clusters in **40 seconds**.
* **Systemic BLASTing:** Rapidly cross-referenced against Human, DEG, and VFDB databases.

---

## 🛠️ Installation

TargetX requires a Linux environment with the following bioinformatics suites:

```bash
# 1. System packages
sudo apt-get update
sudo apt-get install python3-tk

# 2. Clone the repository
git clone https://github.com/cxbl-gbu/TargetX.git
cd TargetX

# 3. Create and activate the environment
conda create -n targetx python=3.10 -y
conda activate targetx

# 4. Install bioinformatics dependencies
conda install bioconda::cd-hit
conda install bioconda::blast==2.16.0

# 5. Install Python dependencies
pip install selenium

#6. Run the Tool
./dist/TargetX

````

---

## 👥 Credits & Authors
TargetX was developed by CxBL (Computational and eXperimental Biomolecular Lab), Gujarat Biotechnology University (GBU).

Meet Parmar – Lead Developer

Soham Bhatt – Bioinformatics Logic & Testing

Dhaval Patel – Supervisor & Principal Investigator

**Affiliation:** Gujarat Biotechnology University (GBU), Gandhinagar, Gujarat, India.

---

## 📄 **License**
This project is licensed under the MIT License.
