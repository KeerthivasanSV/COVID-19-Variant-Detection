# **SARS-CoV-2 Mutation Detection Using Algorithmic Approaches**

This project focuses on analyzing SARS-CoV-2 genomic sequences to detect mutations and understand their evolutionary patterns. Two multiple sequence alignment (MSA) algorithms, **MAFFT (Multiple Alignment using Fast Fourier Transform)** and **PRANK (Probabilistic Alignment Kit)**, are implemented from scratch to detect mutations in SARS-CoV-2 sequences collected from California, Texas, and New York. The study includes sequence alignment, consensus sequence generation, and phylogenetic analysis to explore regional variations and evolutionary divergence.

---

## **Table of Contents**
- [Introduction](#introduction)
- [Objectives](#objectives)
- [Key Features](#key-features)
- [Methodology](#methodology)
  - [Data Collection and Preprocessing](#data-collection-and-preprocessing)
  - [Implementation of MAFFT Algorithm](#implementation-of-mafft-algorithm)
  - [Implementation of PRANK Algorithm](#implementation-of-prank-algorithm)
  - [Phylogenetic Analysis](#phylogenetic-analysis)
  - [Consensus Sequence Comparison](#consensus-sequence-comparison)
- [Results](#results)
- [Technologies Used](#technologies-used)
- [Future Improvements](#future-improvements)
- [Contributors](#contributors)
- [References](#references)

---

## **Introduction**

The COVID-19 pandemic has highlighted the importance of genomic surveillance to monitor viral evolution. SARS-CoV-2, the virus responsible for COVID-19, mutates as it spreads, with some mutations potentially affecting transmissibility, severity, and vaccine efficacy. This project aims to detect these mutations and understand their patterns using computational approaches.

We implement two MSA algorithms—MAFFT and PRANK—from scratch to analyze genomic sequences collected from three U.S. states: California, Texas, and New York. These algorithms are used to align sequences, detect mutations, generate consensus sequences, and construct phylogenetic trees to visualize evolutionary relationships.

---

## **Objectives**

1. Develop MSA-based approaches (MAFFT and PRANK) from scratch for SARS-CoV-2 sequence analysis.
2. Detect mutations and identify conserved regions in SARS-CoV-2 sequences.
3. Compare sequences from California, Texas, and New York to understand regional variations.
4. Construct phylogenetic trees to visualize evolutionary relationships and divergence from the Wuhan reference strain.
5. Generate consensus sequences for each region and analyze their similarities and differences.

---

## **Key Features**

- **Custom MSA Algorithms:** Implementation of MAFFT and PRANK algorithms from scratch for efficient and accurate sequence alignment.
- **Mutation Detection:** Identification of mutation hotspots and conserved regions in SARS-CoV-2 sequences.
- **Regional Analysis:** Comparative analysis of sequences from California, Texas, and New York.
- **Phylogenetic Trees:** Visualization of evolutionary relationships and divergence from the Wuhan reference strain.
- **Consensus Sequences:** Generation of consensus sequences to represent dominant viral strains in each region.

---

## **Methodology**

### **Data Collection and Preprocessing**

1. **Dataset Collection:**
   - Genomic sequences are collected from trusted sources such as GISAID and GenBank.
   - Sequences from California, Texas, and New York are selected for regional analysis.

2. **Data Cleaning:**
   - Sequences are standardized to uppercase and formatted in FASTA.
   - Ambiguous characters are removed, and low-quality sequences are filtered out.

3. **Preprocessing:**
   - Sequences are normalized to the same length.
   - Cleaned datasets are converted into FASTA format for input into alignment algorithms.

---

### **Implementation of MAFFT Algorithm**

MAFFT aligns sequences by converting them into frequency representations using Fast Fourier Transform (FFT). Key steps include:

1. **Numerical Encoding:** Assign numerical values to nucleotides (A=1, C=2, G=3, T=4).
2. **FFT Transformation:** Convert sequences to the frequency domain for efficient comparison.
3. **Similarity Matrix:** Compute pairwise similarities using FFT results.
4. **Guide Tree Construction:** Build a hierarchical clustering tree (UPGMA) for progressive alignment.
5. **Progressive Alignment:** Align sequences following the guide tree order.
6. **Iterative Refinement:** Optimize the alignment by realigning sequences iteratively.

---

### **Implementation of PRANK Algorithm**

PRANK is a phylogeny-aware alignment algorithm that distinguishes between insertions and deletions. Key steps include:

1. **Guide Tree Construction:** Build a phylogenetic tree representing evolutionary relationships.
2. **Indel Handling:** Differentiate between insertions and deletions to improve alignment accuracy.
3. **Phylogeny-Aware Alignment:** Align sequences while considering evolutionary changes.
4. **Posterior Probabilities:** Use probabilistic models to make alignment decisions.

---

### **Phylogenetic Analysis**

1. **Alignment Processing:** Prepare aligned sequences for phylogenetic analysis, including sequence padding and reference strain inclusion.
2. **Distance Calculation:** Compute evolutionary distances between sequences using identity metrics.
3. **Tree Construction:** Build phylogenetic trees using the Neighbor-Joining method.
4. **Tree Visualization:** Visualize evolutionary relationships and identify major clades.

---

### **Consensus Sequence Comparison**

1. **Generation:** Create consensus sequences for each region using majority-rule methods.
2. **Comparison:** Compare consensus sequences to identify similarities and differences.
3. **Identity Matrix:** Construct a matrix summarizing pairwise similarities between regions.

---

## **Results**

1. **MAFFT Results:** High similarity (90.08%) between California and Texas sequences, with New York showing greater divergence.
2. **PRANK Results:** More uniform divergence across all regions, highlighting different evolutionary trajectories.
3. **Phylogenetic Trees:** Visualization of regional clustering and divergence from the Wuhan reference strain.
4. **Consensus Analysis:** Differences in mutation patterns identified across regions.

---

## **Technologies Used**

- **Programming Languages:** Python
- **Libraries and Tools:** NumPy, SciPy, Biopython, Matplotlib
- **Algorithms:** MAFFT, PRANK, Neighbor-Joining
- **Data Formats:** FASTA, CSV
- **Visualization Tools:** Phylogenetic tree construction tools, heatmaps for identity matrices

---

## **Future Improvements**

1. **Algorithm Optimization:** Improve the efficiency of MAFFT and PRANK implementations for large datasets.
2. **Temporal Analysis:** Incorporate time-series data to track mutations over time.
3. **Web Application:** Develop a web interface for real-time mutation detection.
4. **Integration with Clinical Data:** Correlate genomic changes with clinical outcomes.

---

## **Contributors**

- **Abhishek Karthik J (CB.SC.U4AIE23010)**  
- **Keerthivasan S V (CB.SC.U4AIE23037)**  
- **Mothishwaran M P (CB.SC.U4AIE23041)**  
- **Mopuru Sai Bavesh Reddy (CB.SC.U4AIE23044)**  

---

## **References**

1. Katoh, K., et al. (2002). MAFFT: A novel method for rapid multiple sequence alignment using fast Fourier transform. *Nucleic Acids Research*.
2. Löytynoja, A., & Goldman, N. (2005). An algorithm for progressive multiple sequence alignment. *PNAS*.
3. Mercatelli, D., & Giorgi, F. M. (2020). Geographic and genomic distribution of SARS-CoV-2 mutations. *Frontiers in Microbiology*.
4. Hadfield, J., et al. (2018). Nextstrain: Real-time tracking of pathogen evolution. *Bioinformatics*.
