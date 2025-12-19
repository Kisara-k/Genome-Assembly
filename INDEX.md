# Genome Assembly Educational Notebooks - Quick Index

## 📖 Start Here

**New to this series?** Start with [README.md](README.md) for overview, then:

1. **Read notebook descriptions** in README
2. **Start with Notebook 1** (Fundamentals)
3. **Work through in order** (1 → 2 → 3 → 4 → 5)

---

## 📚 Notebooks Overview

### [01_Fundamentals.ipynb](01_Fundamentals.ipynb)

- **Duration**: 4-5 hours
- **Difficulty**: ⭐⭐☆☆☆ (Beginner)
- **Topics**: DNA basics, k-mers, De Bruijn graphs
- **Key Code**: `extract_kmers()`, `SimpleDeBruijnGraph`, `find_eulerian_path()`
- **Output**: Graph visualization, sequence reconstruction
- **Start Here First ✓**

### [02_Read_Preprocessing.ipynb](02_Read_Preprocessing.ipynb)

- **Duration**: 4-5 hours
- **Difficulty**: ⭐⭐⭐☆☆ (Intermediate)
- **Topics**: FASTQ, quality scores, trimming, filtering
- **Key Code**: `parse_fastq()`, `trim_by_quality_sliding_window()`, `complexity_filter()`
- **Output**: Quality plots, preprocessing pipeline results
- **Requires**: Notebook 1 understanding ✓

### [03_Assembly_Algorithms.ipynb](03_Assembly_Algorithms.ipynb)

- **Duration**: 6-8 hours (most important!)
- **Difficulty**: ⭐⭐⭐⭐☆ (Hard)
- **Topics**: Greedy assembly, De Bruijn graphs, error correction
- **Key Code**: `GreedyAssembler`, `DeBruijnAssembler`, algorithm comparison
- **Output**: Assembly results, algorithm benchmark
- **Core Notebook ✓**

### [04_Contigs_and_Scaffolding.ipynb](04_Contigs_and_Scaffolding.ipynb)

- **Duration**: 4-6 hours
- **Difficulty**: ⭐⭐⭐⭐☆ (Hard)
- **Topics**: Contigs, paired reads, scaffolding, gap filling
- **Key Code**: `ContigExtractor`, `Scaffolder`, `GapFiller`, FASTA I/O
- **Output**: Complete assembly pipeline results
- **Requires**: Notebooks 1-3 ✓

### [05_Quality_Assessment.ipynb](05_Quality_Assessment.ipynb)

- **Duration**: 2-3 hours
- **Difficulty**: ⭐⭐⭐☆☆ (Intermediate)
- **Topics**: N50, accuracy, coverage, assembly comparison
- **Key Code**: `calculate_contiguity_metrics()`, `assess_accuracy()`, `detect_repeats_in_assembly()`
- **Output**: Quality metrics, comparison tables, decision trees
- **Wrap Up ✓**

---

## 🎯 By Learning Goal

### "I want to understand assembly concepts"

→ Notebooks 1, 2, 5

### "I want to know how algorithms work"

→ Notebook 3 (most important)

### "I want a complete assembly pipeline"

→ Notebooks 1-4

### "I want to evaluate assembly quality"

→ Notebooks 3, 5

### "I want to compare different assemblers"

→ Notebook 5

---

## 🛠️ By Topic

| Topic               | Notebook | Key Functions                                |
| ------------------- | -------- | -------------------------------------------- |
| K-mers              | 1        | `extract_kmers()`, `count_kmers()`           |
| De Bruijn Graph     | 1, 3     | `SimpleDeBruijnGraph`, `DeBruijnGraph`       |
| Quality Scores      | 2        | `phred_to_error_prob()`, `analyze_quality()` |
| Trimming            | 2        | `trim_by_quality_sliding_window()`           |
| Adapter Removal     | 2        | `find_adapter_end()`, `trim_adapters()`      |
| Greedy Assembly     | 3        | `GreedyAssembler.assemble()`                 |
| De Bruijn Assembly  | 3        | `DeBruijnAssembler.assemble()`               |
| Error Correction    | 3        | Graph simplification, min coverage           |
| Contigs             | 4        | `ContigExtractor.extract_contigs()`          |
| Scaffolding         | 4        | `Scaffolder.build_scaffold_links()`          |
| Gap Filling         | 4        | `GapFiller.find_path()`                      |
| N50 Calculation     | 5        | `calculate_contiguity_metrics()`             |
| Coverage Analysis   | 5        | `analyze_coverage()`                         |
| Repeat Detection    | 5        | `detect_repeats_in_assembly()`               |
| Assembly Comparison | 5        | `compare_assemblies()`                       |

---

## ⏱️ Time Estimates

**Total time to complete all notebooks:**

- Beginner: 25-35 hours
- Intermediate: 20-25 hours
- Advanced: 15-20 hours

**Per notebook:**

- Notebook 1: 4-5 hours (concepts)
- Notebook 2: 4-5 hours (practical)
- Notebook 3: 6-8 hours (algorithms - hardest!)
- Notebook 4: 4-6 hours (pipeline)
- Notebook 5: 2-3 hours (evaluation)

---

## 🔬 Hands-On Exercises

Each notebook includes:

- ✓ Runnable code examples
- ✓ Synthetic data generation
- ✓ Visualization of results
- ✓ Suggestions to modify and re-run
- ✓ Real data source guidance

**To get the most out of these:**

1. Read markdown cells carefully
2. Run code cells in order
3. Predict output before running
4. Modify parameters and experiment
5. Try to break things (and fix them!)

---

## 🔗 Connecting to External Tools

### Real Assemblers (Used in Production)

- **SPAdes** (short reads, default): `conda install spades`
- **FLYE** (long reads): `conda install flye`
- **Canu** (long reads, accurate): `conda install canu`
- **Velvet** (original De Bruijn): `conda install velvet`

### Quality Assessment

- **QUAST**: Full assembly evaluation
- **BUSCO**: Completeness check
- **AssemblyStats**: Simple statistics

### Data Download

- **SRA Toolkit**: `conda install sra-tools`
- Command: `fasterq-dump SRR1234567 -O reads/`

---

## 📊 Complexity Levels

```
Easy   [1: Fundamentals] ━━━━━━━━━━━━━━━━━━━━━━━━
Hard   [2: Preprocessing] ━━━━━━━━━━━━━━━━━━━━━━━
Very   [3: Algorithms] ━━━━━━━━━━━━━━━━━━━━━━━━━━
Hard   [4: Scaffolding] ━━━━━━━━━━━━━━━━━━━━━━━━
       [5: Quality] ━━━━━━━━━━━━━━━━━━━━━━━

Legend: ━ = 1 hour equivalent
```

Notebook 3 is the hardest - it has the most important concepts!

---

## ❓ Common Questions

**Q: Can I skip notebooks?**
A: Not recommended. Notebook 3 requires concepts from 1-2. Start from the beginning.

**Q: How much Python do I need?**
A: Intermediate level. You should understand classes, functions, loops, dictionaries.

**Q: Do I need biology knowledge?**
A: No - all concepts explained from scratch!

**Q: Can I run these on my laptop?**
A: Yes! Synthetic examples in notebooks are fast. Real large genomes need servers.

**Q: Which notebook is most important?**
A: **Notebook 3** (Assembly Algorithms) - it explains WHY modern methods work.

---

## 🎓 Learning Path Recommendations

### Path A: Fast Learner (15-20 hours)

- Read markdown carefully
- Run code, don't modify much
- Focus on notebooks 1, 3, 5
- Good for: Getting overview, job interviews

### Path B: Balanced Learner (25-30 hours)

- Read everything
- Run and modify code
- All 5 notebooks in order
- Good for: Solid understanding, future work

### Path C: Deep Diver (35+ hours)

- Deep dive into each notebook
- Implement variations
- Run on real data from SRA
- Good for: Mastery, research work

---

## 🚀 Getting Started Now

### Minimum Setup

```bash
# 1. Install Python and Jupyter
conda create -n genome python=3.10 jupyter
conda activate genome

# 2. Install required packages
conda install numpy matplotlib scipy

# 3. Open notebooks
jupyter notebook
```

### Recommended Setup

```bash
# Same as above, plus:
conda install -c bioconda spades flye  # Real tools (optional)
conda install -c bioconda sra-tools    # Download real data (optional)
```

---

## 📚 Reading Guide

### For Each Notebook:

1. **Start with README.md** - Overview of series
2. **Read title and overview** - What's this about?
3. **Read markdown cells** - Understand concepts
4. **Run code cells** - See it in action
5. **Modify and experiment** - Deeper learning
6. **Try exercises** - Practice understanding

### Key Sections to Highlight:

- "Why this matters" sections
- Algorithm comparisons
- Real data guidance
- Troubleshooting tips

---

## ✅ Completion Checklist

- [ ] Notebook 1: Understand k-mers and graphs
- [ ] Notebook 2: Can process real FASTQ files
- [ ] Notebook 3: Implemented both greedy and De Bruijn
- [ ] Notebook 4: Can run complete assembly pipeline
- [ ] Notebook 5: Can evaluate and compare assemblies
- [ ] README: Understand when to use each tool
- [ ] SUMMARY: Know what you learned

**Once complete:** You understand genome assembly! 🎉

---

## 📞 Support

**Having trouble?**

1. Check the FAQ in README.md
2. Look for similar code in other notebooks
3. Modify parameters and see what changes
4. Read docstrings (they explain everything!)

**Want to learn more?**

- Read papers listed in README
- Try notebooks with real data
- Implement your own improvements
- Compare with published tools

---

**Ready to start? Open [01_Fundamentals.ipynb](01_Fundamentals.ipynb) now!** 🚀

(Or read [README.md](README.md) first if you want more context.)
