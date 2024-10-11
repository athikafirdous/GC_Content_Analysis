## GC_Content_Analysis
``R script to calculate GC content in DNA sequences``
## Function to calculate GC content
``calculate_gc_content <- function(dna_sequence) {``
  
  ## Convert the sequence to uppercase to avoid mismatches
  ``dna_sequence <- toupper(dna_sequence)``
  
  ## Count the number of G's and C's in the sequence
 `` g_count <- sum(strsplit(dna_sequence, NULL)[[1]] == "G")``
 `` c_count <- sum(strsplit(dna_sequence, NULL)[[1]] == "C")``
  
  ## Total length of the sequence
 `` total_length <- nchar(dna_sequence)``
  
  ## Calculate the GC content as a percentage
 `` gc_content <- ((g_count + c_count) / total_length) * 100``
  
 `` return(gc_content)
}``

## Example DNA sequence
``example_sequence <- "AGCTGCGCGTTAGC"``

## Calculate GC content for the example sequence
``gc_content <- calculate_gc_content(example_sequence)``

## Print the result
``cat("GC Content:", gc_content, "%\n")``

