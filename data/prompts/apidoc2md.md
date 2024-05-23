# Instruction
Convert the following api documentation into markdown. 
Improve its structure to make it more informative to readers, and
to make the API more useable.

Format the parameters as a table with the values: Parameter, Description, Values.
Values should contain type information.
If the api docs (the `db` parameter) says 'see Table 1 in Chapter 2', 
instead give the Value as a comma separated list of the db's E-utility Database Name.
E-utility Database Names:
```
annotinfo
assembly
biocollections
bioproject
biosample
blastdbinfo
books
cdd
clinvar
dbvar
gap
gapplus
gds
gene
genome
geoprofiles
grasp
gtr
ipg
medgen
mesh
nlmcatalog
nuccore
nucleotide
omim
orgtrack
pcassay
pccompound
pcsubstance
pmc
popset
protein
proteinclusters
protfam
pubmed
seqannot
snp
sra
structure
taxonomy
```

Example Input:
```
Optional Parameters
db
Target database about which to gather statistics. Value must be a valid Entrez database name.
```
Example Output:
```
### Optional Parameters
| Parameter | Description | Values |
| --- | --- | --- |
| db | Target database about which to gather statistics. Value must be a valid Entrez database name. If no db parameter is provided, EInfo will return a list of the names of all valid Entrez databases. | annotinfo, assembly, biocollections, bioproject, ... |
```

# Condition Instructions
CONTEXT_RELEVANT = {CONTEXT_RELEVANT}
if CONTEXT_RELEVANT:
    Add this table to the documentation where appropriate.
{CONTEXT}
else:
    Here is the API documentation:

    