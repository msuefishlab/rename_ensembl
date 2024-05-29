conda activate seqkit



1. Download the Species Lookup List from (http://useast.ensembl.org/info/genome/stable_ids/prefixes.html) => species_lookup_new.txt

2. Download Alignment from ENSEMBL (FASTA Format)

3. Run the following commands:

  conda activate seqkit
  seqkit replace -p '(^ENS[A-Z]{3})' -r '{kv} $1' -k species_lookup_new.txt danio_orthologs.fa.txt --keep-key > CFAP_orthologs.fa

4. Profit!
