# BME_Assignment
# Protein 2D Structure Prediction
1. Data Preprocessing

-FASTA download: Protein sequences are automatically fetched from NCBI using accession IDs.

-Parsing: Each sequence is tokenized into integers using a vocabulary of 20 standard amino acids.

-Pseudo-labeling: Secondary structures are assigned via a rule-based sliding window heuristic:

  ->H (Helix) if helix-preferring residues dominate.

  ->E (Strand) if strand-preferring residues dominate.

  ->C (Coil) otherwise.

-Dataset Split: Data is split into Train (70%), Validation (15%), and Test (15%) loaders with dynamic padding.
