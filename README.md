# 🧬 DNA Sequence Alignment using Genetic Algorithm

> A Python-based Final Year Project that applies a Genetic Algorithm (GA) to find the optimal alignment between DNA sequences — mimicking how nature evolves toward the best solution.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [How It Works — The Genetic Algorithm](#how-it-works--the-genetic-algorithm)
- [Project Structure](#project-structure)
- [Installation & How to Run](#installation--how-to-run)
- [Results & Output](#results--output)
- [References](#references)

---

## Project Overview

DNA sequence alignment is the process of arranging two or more DNA sequences to identify regions of similarity. This project uses a **Genetic Algorithm (GA)** — an optimization technique inspired by biological evolution — to search for the best possible alignment between DNA sequences.

Instead of checking every possible alignment (which is computationally expensive), the GA evolves a population of candidate alignments over multiple generations, gradually improving toward the optimal solution.

**Key features:**
- Encodes DNA alignment as chromosomes in a population
- Uses fitness scoring based on sequence match quality
- Applies selection, crossover, and mutation operators
- Outputs the best alignment found across generations

---

## How It Works — The Genetic Algorithm

The GA mimics the process of natural selection. Here's how each stage maps to the DNA alignment problem:

```
Initial Population
      │
      ▼
 Fitness Evaluation  ◄──────────────────┐
 (Score each alignment)                 │
      │                                 │
      ▼                                 │
 Selection                              │
 (Choose the best alignments)           │
      │                                 │
      ▼                                 │
 Crossover                              │
 (Combine two alignments → offspring)   │
      │                                 │
      ▼                                 │
 Mutation                               │
 (Randomly tweak an alignment)          │
      │                                 │
      ▼                                 │
 New Generation  ────────────────────────┘
      │
      ▼
 Best Alignment Found ✅
```

| GA Concept     | In This Project                                      |
|----------------|------------------------------------------------------|
| Chromosome     | A candidate DNA alignment (sequence with gaps)       |
| Gene           | A single nucleotide position (A, T, G, C, or `-`)    |
| Fitness        | Match score — higher matches = higher fitness        |
| Selection      | Tournament or roulette-wheel selection               |
| Crossover      | Single-point or two-point crossover of alignments   |
| Mutation       | Randomly insert/remove a gap in the alignment       |

---

## Project Structure

```
dna-sequence-genetic-algorithm/
│
├── main.py                  # Entry point — run this file
├── genetic_algorithm.py     # Core GA logic (selection, crossover, mutation)
├── fitness.py               # Fitness function for scoring alignments
├── dna_utils.py             # DNA sequence utilities and helpers
├── config.py                # Parameters (population size, mutation rate, etc.)
│
├── data/
│   └── sequences.txt        # Input DNA sequences
│
├── results/
│   └── best_alignment.txt   # Output — best alignment found
│
├── requirements.txt
└── README.md
```

---

## Installation & How to Run

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Step 1 — Clone the repository

```bash
git clone https://github.com/your-username/dna-sequence-genetic-algorithm.git
cd dna-sequence-genetic-algorithm
```

### Step 2 — Install dependencies

```bash
pip install -r requirements.txt
```

### Step 3 — Configure parameters (optional)

Open `config.py` to adjust the GA settings:

```python
POPULATION_SIZE  = 100      # Number of candidate alignments per generation
GENERATIONS      = 500      # How many generations to evolve
MUTATION_RATE    = 0.01     # Probability of a mutation occurring
CROSSOVER_RATE   = 0.8      # Probability of crossover between parents
```

### Step 4 — Run the project

```bash
python main.py
```

### Step 5 — View results

The best alignment will be printed to the console and saved in `results/best_alignment.txt`.

---

## Results & Output

After running the algorithm, you will see output similar to:

```
Generation 1   | Best Fitness: 42.3
Generation 50  | Best Fitness: 67.8
Generation 200 | Best Fitness: 89.1
Generation 500 | Best Fitness: 96.4

✅ Best Alignment Found:
Sequence 1:  ATCG--TAGCTA
Sequence 2:  ATCGTA--GCTA
Score: 96.4%
```

> **Note:** Add screenshots of your plots or terminal output here once your project is complete. You can drag and drop images directly into the GitHub README editor.

---

## References

1. Holland, J. H. (1975). *Adaptation in Natural and Artificial Systems*. University of Michigan Press.
2. Needleman, S. B., & Wunsch, C. D. (1970). A general method applicable to the search for similarities in the amino acid sequence of two proteins. *Journal of Molecular Biology*, 48(3), 443–453.
3. Mitchell, M. (1998). *An Introduction to Genetic Algorithms*. MIT Press.
4. Goldberg, D. E. (1989). *Genetic Algorithms in Search, Optimization, and Machine Learning*. Addison-Wesley.
5. Biopython Documentation — https://biopython.org/docs/

---

## 👩‍💻 Author

**Ayesha** — Final Year Project, [Agriculture University]  
📧 your-email@university.edu  
🔗 [GitHub Profile](https://github.com/ayeshaparacha6692-design/dna-sequence-genetic-algorithm.git)

---

*This project was developed as part of a Final Year Project requirement.*
