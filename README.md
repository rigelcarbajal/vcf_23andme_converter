# 🧬 VCF to 23andMe v5 Converter

This script converts a standard VCF (Variant Call Format) file into a 23andMe-like plain text format (version 5 style), suitable for use in personal genetic analysis platforms.

✅ **Features**
-	Supports VCF files aligned to hg19/GRCh37.
-	Filters and includes only valid SNPs with known rsIDs.
-	Converts genotypes into the 23andMe format (e.g., AA, CT, etc.).
-	Ensures chromosome naming follows 23andMe conventions (1–22, X, Y, MT).
-	Adds metadata headers for compatibility and clarity.
-	Performs basic input validation to avoid formatting issues.

📥 **Input**
-	A VCF file (e.g., input.vcf) containing SNP data with at least one sample column.

📤 **Output**
-	A tab-delimited .txt file (e.g., 23andme_dna.txt) with the following columns:
 ```text
rsid  chromosome  position  genotype
```

🔧 **Usage**
```bash
python vcf_to_23andme.py input.vcf output.txt
```

🧠 **Notes**
- If your VCF is aligned to hg38, you’ll need to perform liftover to hg19 using tools like [UCSC liftOver](https://genome.ucsc.edu/cgi-bin/hgLiftOver).
- This script is for educational and research use only. It is not affiliated with 23andMe.
