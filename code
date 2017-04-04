# Start by setting up the variables
# x and y are used to go through the sequence in codons, in order to replace codons in a sequential, end-to-end fashion
# Start tells where to start the translation process
# Codon will be the variable that contains the sequence of codons from the user DNA input

dna_input = raw_input("Welcome to the DNA > Protein Machine. Please enter your DNA sequence, from 5'> 3'. ").upper()
start = 0
x = 0
y = 3	
codon =""
import re

# We want the user input to be specifically nucleotides A,T,G and C with proper number of nucleotides
# The following loops will deal to format something like "ATGCAT" into "ATG CAT" so that we only deal with the first reading frame

while True:
	if len(dna_input) % 3 == 0 and re.search(r"[^ATGC]", str(dna_input)) == None:
		dna_sequence = str(dna_input)
	else:
		dna_input = raw_input("Please make sure to consider reading frames. Fix improper codons (i.e. Your code cannot contain 1 or 2 nucleotide long codons) before you continue. No spaces or irrelevant characters.").upper()
		exit()
		break

	while True:
		if start < len(dna_sequence):			
			codon = str(codon) + " " + str(dna_sequence[x:y])
			x = x+3
			y = y+3
			start = start + 3
		else:
			break

# This will let us convert the dna sequence into a sequence of amino acids

	mod_dna_sequence = str(codon)

	amino_acids = mod_dna_sequence.replace("TTT","Phe").replace("TTC","Phe").replace("TTA","Leu").replace("TTG","Leu").replace("CTT","Leu").replace("CTC","Leu").replace("CTA","Leu").replace("CTG","Leu").replace("ATT","Ile").replace("ATC","Ile").replace("ATA","Ile").replace("ATG","Met").replace("GTT","Val").replace("GTC","Val").replace("GTA","Val").replace("GTG","Val").replace("TCT","Ser").replace("TCC","Ser").replace("TCA","Ser").replace("TCG","Ser").replace("CCT","Pro").replace("CCC","Pro").replace("CCA","Pro").replace("CCG","Pro").replace("ACT","Thr").replace("ACC","Thr").replace("ACA","Thr").replace("ACG","Thr").replace("GCT","Ala").replace("GCC","Ala").replace("GCA","Ala").replace("GCG","Ala").replace("TAT","Tyr").replace("TAC","Tyr").replace("TAA","STOP").replace("TAG","STOP").replace("CAT","His").replace("CAC","His").replace("CAA","Gln").replace("CAG","Gln").replace("AAT","Asn").replace("AAC","Asn").replace("AAA","Lys").replace("AAG","Lys").replace("GAT","Asp").replace("GAC","Asp").replace("GAA","Glu").replace("GAG","Glu").replace("TGT","Cys").replace("TGC","Cys").replace("TGA","STOP").replace("TGG","Trp").replace("CGT","Arg").replace("CGC","Arg").replace("CGA","Arg").replace("CGG","Arg").replace("AGT","Ser").replace("AGC","Ser").replace("AGA","Arg").replace("AGG","Arg").replace("GGT","Gly").replace("GGC","Gly").replace("GGA","Gly").replace("GGG","Gly")
	
	print"The corresponding amino acid sequence is: "
	
	print amino_acids
	exit()
