# VarnerLab_Minimizing_Tn_Antigen
Part of my CHEME7770 project, and also a small part of my thesis work (not completely)

This file has source code for CHEME7770 Project- "Minimization of Tn and T antigen production by Metabolic Flux Balance Analysis"


Acknowledgements

Thanking VarnerLab for allowing us to use files in src. 
Coding of the all matlab files done by Aravind Sureshbabu (as2625)


How to run the FBA for your own system of interest

1) If you are performing TX/TL reactions for gene of interest, download the nucleotide sequence and protein sequence in .txt format. Keep it in the 
GENE FASTA Folder
2) Run the Template.m file to generate the set of TXTL reactions for gene of interest. Output will be stored as a .txt file containing the reactions
3) Open Model. Open Stoich.jl. You can enter in the reactions. Run Stoich.jl. 
4) Output Matrix is saved as Matrix.txt
5) Go to constants.m to modify the parameters. If you are modifying the parameter, make sure to modify the corresponding flux in bounds.m
6) Change the annotated places in Optimizer.m. Uncomment lines and run the program. 

Files present in the repository and Folders Present

1) GENE FASTA- Contains the FASTA files for gene of interest

geneSequence.m- Used for generating triphosphate count. Main purpose to generate strings for Template.m. Modify file name as per FASTA name
nucleotideCount.m- Used for generating ATGC content. Main purpose to generate strings for Template.m. Modify file name as per FASTA name
Template.m- Generates the reaction set for TXTL

2) Model
a) src- Contains auxillary files needed for Stoich_calculation.jl - DONOT MODIFY ANY OF THESE FILES

a-1) Expa.jl- Generates the extreme pathway analysis
a-2) Include.jl- Driver file needed for Stoich_calculation.jl
a-3)Parser.jl- Need for reaction frequency 
a-4) Stoichiometric.jl- Need to get S matrix


bounds.m- Contains the flux bounds
constraints.m- Contains the TXTL values 
Optimizer.m- The optimizer 

SourceCode

Contains the files that are in Model, for 4 systems of interest
