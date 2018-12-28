POM (Primer of molecular markers) 1.00 help

System and software requirements:
Operating Systems: Window 7,8,10 / Linux(Ubuntu, CentOS) / Mac OS
Software libraries and versions: Java runtime environments 1.7 or later

Input data:  (i) Genome sequence file in FASTA format. (ii) Indels file for Indels primer design in VCF (Variant Call Format). (iii) SNPs and Indels files for exclusion from primers in VCF.

Output data: The main output file is primer list file with checking variation in primer and specificity in tab format. Other files are k-mer position file, SSRs list file, SSRs summary file, primer3 input and output file, and primer list file without checking.


User interface use case:
1 Double click PomUI.jar to run the POM user interface.
2 Select Common Setting panel to change parameters and Select SNP/Indel vcf for exclusion.
3 Select Indels or SSRs primer design panel and select genome fasta and indel vcf.
4 Click start button and waiting for finish.
5 view result in Viewer panel.
6 double click primer pairs in result list to view the products.

Command line use case:
Assuming that you extract sample data in disk D.

1. For Indels primer design:
java -jar PrimerOfMarkers1.25.jar -fun indel -file D:\SampleData\Tair10.1.fasta -posFile D:\SampleData\indels_4_primer.vcf -varpreexclusion yes -varfinalcheck yes -snplistfile D:\SampleData\all10_snps.vcf -indellistfile D:\SampleData\all10_indels.vcf

2. For SSRs primer design:
java -jar PrimerOfMarkers1.25.jar -fun ssr -file D:\SampleData\Tair10.1.fasta -varpreexclusion yes -varfinalcheck yes -snplistfile D:\SampleData\all10_snps.vcf -indellistfile D:\SampleData\all10_indels.vcf

3. For viewing product information:
java -jar PrimerOfMarkers1.25.jar -fun view -file D:\SampleData\POM\Tair10.1.fasta.fasta -result D:\SampleData\POM\Tair10.1.fasta.fasta.Indel.PrimerAllLsWithCheck.xls -line 16 -snplistfile D:\SampleData\I_10001_SNP.vcf -indellistfile D:\SampleData\I_10001_Indel.vcf
