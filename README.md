# Experiment 6: MapReduce Word Count Simulator

Simulates the fundamental phases of the MapReduce programming model (**Map**, **Shuffle & Sort**, and **Reduce**) in Java.

---

## 🚀 Execution Commands

Run the following commands in the project directory:

```bash
# 1. Compile the Java program
javac WordCountSimulator.java

# 2. Run the compiled program
java WordCountSimulator
```

> **Note:** If single-step execution is supported in your environment (Java 11+), you can also run:
> ```bash
> java WordCountSimulator.java
> ```

---

## 🔄 Execution Sequence

1. **Input Phase:** Reads sample documents / text lines.
2. **Map Phase:** Tokenizes each line and generates `(word, 1)` intermediate pairs.
3. **Shuffle & Sort Phase:** Groups values by word in alphabetical order `(word, [1, 1, ...])`.
4. **Reduce Phase:** Aggregates counts for each distinct word and outputs the final frequencies.

---

## 📊 Example Output

```text
--- Input Documents ---
> Distributed computing systems enable concurrent computation.
> MapReduce simplifies big data processing.
> Word count is the standard hello world of distributed MapReduce.

--- Intermediate Mapped Pairs (Sample) ---
(distributed, 1)
(computing, 1)
(systems, 1)
(enable, 1)
(concurrent, 1)
(computation, 1)

--- Final Word Counts (Reduce Output) ---
Word                 | Count
---------------------|-------
big                  | 1
computation          | 1
computing            | 1
concurrent           | 1
count                | 1
data                 | 1
distributed          | 2
enable               | 1
hello                | 1
is                   | 1
mapreduce            | 2
of                   | 1
processing           | 1
simplifies           | 1
standard             | 1
systems              | 1
the                  | 1
word                 | 1
world                | 1
```
