#Running arlequin to test for outliers
#did this analysis twice, once with natural pops and a second time with ALL pops
#steps taken in the natural pops analysis:

1) hand format genepop (3 digit code) for input to .py conversion to 2 digit 

2) convert genepop (3 digit code) to genepop (2 digit code) using:
	script: convert_genepop-3to2_digit_code.mb.py
	in: I:\WAE_RAD_Data\STACKS_publish\phase2-pop_Gen\SNPS\v6_SNPs_3to2_digit_in.gen
	out: I:\WAE_RAD_Data\STACKS_publish\phase2-pop_Gen\SNPS\v6_SNPs_natural_pops_2_digit.gen
	NOTE: hand format output according to notes in .py (add SNP names back)
	
2) convert genepop to arlequin format using:
	script: genepop2arlequin.slurm
	.gen: v6_SNPs_natural_pops_2_digit.gen
	.spid: genepop2arlequin.spid
	out: v6_SNPs_natural_pops.arl
	
	
3)run arlequin analyses:
NOTE: To get arlequi to open project when I ran "start", I had to make sure the data type was titled "STANDARD"

NOTE: first must hand edit the structure setup. grouping used is as follows:
	Delavan:	3
	Lake_Wisconsin:	1
	Big_arb:	1
	Chip_flow:	2
	Cutfoot:	6
	Eau_C:	2
	Kawague:	1
	Lake_Koronis:	7
	Maniowish:	2
	Medicine:	1
	Mille_Lacs:	8
	Otter:	9
	Pike:	5
	Pine:	10
	Red:	11
	Sarah:	12
	St_Lo:	13
	Turtle_F:	2
	Willow:	1
	Wolf:	4
	

	3.a) AMOVA (locus by locus)
	3.b) outlier test (hierarchical island model)
	3.c) Pairwise FST (default)
	
	
	in: 
	settings: 
	out: 
	
#ALL Pops analysis
same steps as the natural pops except I've now modified the 3 digit to 2 digit .py script so that you don't need to format it by hand,
just plug and play!



