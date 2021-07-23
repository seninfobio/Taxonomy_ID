# Taxonomy_ID

How to find Taxonomy ID, form the out put of blastx
why!, Using the taxonomy id can identify the homologous speices 

[Solution](https://www.biostars.org/p/367121/)

[NCBI_enterz_conda](https://anaconda.org/bioconda/entrez-direct)

eg.
```bash
$ esearch -db nuccore -query "NG_047018" | elink -target taxonomy | efetch -format native -mode xml | grep ScientificName | awk -F ">|<" 'BEGIN{ORS=", ";}{print $3;}'

Homo sapiens, cellular organisms, Eukaryota, Opisthokonta, Metazoa, Eumetazoa, Bilateria, Deuterostomia, Chordata, Craniata, Vertebrata, Gnathostomata, Teleostomi, Euteleostomi, Sarcopterygii, Dipnotetrapodomorpha, Tetrapoda, Amniota, Mammalia, Theria, Eutheria, Boreoeutheria, Euarchontoglires, Primates, Haplorrhini, Simiiformes, Catarrhini, Hominoidea, Hominidae, Homininae, Homo,

```

