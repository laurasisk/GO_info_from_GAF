# GO_info_from_GAF
Extract GO term descriptors from GAF. Useful for non-model/non-ensembl genomes. 

## Download ontogeny ID to descriptor file (go.obo) from https://lpalbou.github.io/docs/download-ontology/
```
wget http://purl.obolibrary.org/obo/go.obo
```

```
wget https://current.geneontology.org/ontology/go.json

```

The file contents look something like:
Term]
id: GO:0000002
name: mitochondrial genome maintenance
namespace: biological_process
def: "The maintenance of the structure and integrity of the mitochondrial genome; includes replication and segregation of the mitochondrial chromosome." [GOC:ai, GOC:vw]
is_a: GO:0007005 ! mitochondrion organization


## Download the GAF file for your genome from the http
