# Genome Assembly: From Reads to Genomes

A comprehensive educational series of Jupyter notebooks teaching genome assembly algorithms from first principles. Designed for people comfortable with coding and algorithms but new to genomics.

## 📚 Notebook Series

### [1. Fundamentals](01_Fundamentals.ipynb)

**What you'll learn:**

- DNA sequence basics and representation
- Next-generation sequencing (NGS) reads and quality scores
- K-mers: the building blocks of modern assembly
- De Bruijn graphs: the core data structure
- How perfect assembly would work with an Eulerian path
- Why sequencing errors and repeats make assembly hard

---

### [2. Read Preprocessing & Quality Control](02_Read_Preprocessing.ipynb)

**What you'll learn:**

- How to read and analyze FASTQ files
- Quality assessment and visualization
- Adapter trimming and quality-based trimming
- Complexity filtering and deduplication
- Complete preprocessing pipeline with real data sources

---

### [3. De Novo Assembly Algorithms](03_Assembly_Algorithms.ipynb)

**What you'll learn:**

- **Greedy Overlap Assembly**: Simple but slow O(n²) algorithm
- **De Bruijn Graph Assembly**: Modern, fast O(n) approach
- **Algorithm Comparison**: Both implemented and benchmarked
- **Key insight:** De Bruijn graphs are ~100x faster

---

### [4. Contigs and Scaffolding](04_Contigs_and_Scaffolding.ipynb)

**What you'll learn:**

- Contig extraction from graph paths
- Paired-end reads and insert size estimation
- Scaffolding algorithm: linking contigs using pair information
- Gap filling between contigs
- Complete assembly pipeline from reads to scaffolds

---

### [5. Assembly Quality Assessment](05_Quality_Assessment.ipynb)

**What you'll learn:**

- **Contiguity metrics**: N50, L50, N75, N90
- **Accuracy assessment** against reference genomes
- **Coverage analysis** and repeat resolution
- **Comparing assemblies**: which is better?
- **Choosing assemblers**: decision tree by organism type

---

## 🔧 Installation

```bash
# Using conda (recommended)
conda create -n genome-assembly python=3.10 jupyter numpy matplotlib scipy
conda activate genome-assembly

# Launch Jupyter
jupyter notebook
```

**Requirements:**

- Python 3.8+
- numpy, matplotlib, scipy
- Jupyter Notebook

---

## 🚀 Getting Started

1. Open `01_Fundamentals.ipynb` first
2. Work through notebooks 1-5 in order
3. Run each cell sequentially
4. Try modifying parameters and re-running
5. (Optional) Use real data from SRA for advanced practice

---

## 📊 Workflow Overview

```
Sequencing Data (FASTQ)
        ↓
[Preprocessing] → Clean reads
        ↓
[Assembly] → Contigs
        ↓
[Scaffolding] → Scaffolds
        ↓
[Quality Assessment] → Report
```

---

## 💡 Key Concepts

- **K-mers**: Short DNA sequences used as building blocks
- **De Bruijn Graph**: Data structure encoding k-mer overlaps
- **Contig**: Contiguous sequence (unambiguous path in graph)
- **Scaffold**: Contigs linked by paired-read information
- **N50**: Most important quality metric (higher is better)

---

## 📖 Data Sources

- **NCBI SRA**: https://www.ncbi.nlm.nih.gov/sra
- **ENA**: https://www.ebi.ac.uk/ena
- **PATRIC**: https://www.patricbrc.org/

Notebooks include guides for downloading real data.

---

## 🎯 Learning Outcomes

After completing this series, you will understand:

- How genome sequencing produces reads
- Why assembly is fundamentally hard
- How De Bruijn graphs solve the problem
- Modern assembly algorithms and their trade-offs
- How to evaluate assembly quality
- When to use different assemblers

---

## ❓ FAQ

**Do I need a biology background?**
No - all concepts are explained. Just need comfort with coding and algorithms.

**Can I run this on a laptop?**
Yes - synthetic examples are fast. Real large genomes need more resources.

**Why implement algorithms instead of using tools?**
Understanding the concepts is more valuable than using a black box. Real work would use SPAdes or FLYE.

**How much time?**
20-30 hours reading + 10-20 hours hands-on coding.

---

Made with ❤️ for learning bioinformatics
