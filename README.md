# GO_info_from_GAF
Extract GO term descriptors from GAF. Useful for non-model/non-ensembl genomes. 

# Environment:
Python 3.9.14


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
Example:
```
wget https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/001/970/005/GCF_001970005.1_Flounder_ref_guided_V1.0/GCF_001970005.1_Flounder_ref_guided_V1.0_gene_ontology.gaf.gz
```

Then unzip the file

```
gunzip GCF_001970005.1_Flounder_ref_guided_V1.0_gene_ontology.gaf.gz   

```

The file contents will look like this:
#DB    GeneID  Symbol  Qualifier       GO_ID   Reference       Evidence_Code   With,From       Aspect  Gene_Name       Gene_Synonym    Type    Taxon   Date    Assigned_By     Annot_Ext       Gene_Product_Form_ID
NCBIGene        109623492       tmem35a located_in      GO:0005783      PMID:30032202   IEA     UniProtKB:H2L7F3        C       NA      
        protein taxon:8255      20231104        RefSeq          
NCBIGene        109623492       tmem35a enables GO:0030548      PMID:30032202   IEA     UniProtKB:H2L7F3        F       NA              protein taxon:8255      20231104        RefSeq          
NCBIGene        109623492       tmem35a involved_in     GO:0051131      PMID:30032202   IEA     UniProtKB:H2L7F3        P       NA      
        protein taxon:8255      20231104        RefSeq          
NCBIGene        109623492       tmem35a involved_in     GO:2000010      PMID:30032202   IEA     UniProtKB:H2L7F3        P       NA      
        protein taxon:8255      20231104        RefSeq          

