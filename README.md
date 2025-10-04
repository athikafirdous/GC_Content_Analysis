# 🧬 GC Content Analysis
![Made with R](https://img.shields.io/badge/Made%20with-R-blue?logo=r&logoColor=white)

A simple **R script** to calculate the GC content of DNA sequences.  
This project demonstrates a basic **bioinformatics analysis** for understanding nucleotide composition in genomic data.

---

## 📘 Overview

GC content refers to the percentage of **guanine (G)** and **cytosine (C)** bases in a DNA sequence.  
This script:
- Takes a DNA sequence as input.
- Calculates the GC percentage.
- Outputs the result to the console.

---

## 🧩 Function: `calculate_gc_content()`

```r
calculate_gc_content <- function(dna_sequence) {
  # Convert sequence to uppercase
  dna_sequence <- toupper(dna_sequence)
  
  # Count G's and C's
  g_count <- sum(strsplit(dna_sequence, NULL)[[1]] == "G")
  c_count <- sum(strsplit(dna_sequence, NULL)[[1]] == "C")
  
  # Calculate GC%
  total_length <- nchar(dna_sequence)
  gc_content <- ((g_count + c_count) / total_length) * 100
  
  return(gc_content)
}

# Example DNA sequence
example_sequence <- "AGCTGCGCGTTAGC"

# Calculate GC content
gc_content <- calculate_gc_content(example_sequence)

# Print result
cat("GC Content:", gc_content, "%\n")

## Sample Output 
GC Content: 57.14286 %

🧑‍💻 Author

Athika Firdous
MSc Bioinformatics | Jamia Millia Islamia
📫 [GitHub Profile](https://github.com/athikafirdous)


---

📄 License

This project is open-source and available under the MIT License.


---

💬 Contributing

Contributions and improvements are welcome!
Feel free to fork the repository and submit a pull request.
