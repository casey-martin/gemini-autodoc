### Table 1: Valid values of &retmode and &rettype for EFetch (null = empty string)

#### All Databases
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| Document summary | docsum | xml, default |
| List of UIDs in XML | uilist | xml |
| List of UIDs in plain text | uilist | text |

#### db = bioproject
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| Full record XML | xml, default | xml, default |

#### db = biosample
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| Full record XML | full, default | xml, default |
| Full record text | full, default | text |

#### db = gds
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| Summary | summary, default | text, default |

#### db = gene
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| text ASN.1 | null | asn.1, default |
| XML | null | xml |
| Gene table | gene_table | text |

#### db = homologene
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| text ASN.1 | null | asn.1, default |
| XML | null | xml |
| Alignment scores | alignmentscores | text |
| FASTA | fasta | text |
| HomoloGene | homologene | text |

#### db = mesh
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| Full record | full, default | text, default |

#### db = nlmcatalog
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| Full record | null | text, default |
| XML | null | xml |

#### db = nuccore, protein or popset
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| text ASN.1 | null | text, default |
| binary ASN.1 | null | asn.1 |
| Full record in XML | native | xml |
| Accession number(s) | acc | text |
| FASTA | fasta | text |
| TinySeq XML | fasta | xml |
| SeqID string | seqid | text |

#### Additional options for db = nuccore or popset
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| GenBank flat file | gb | text |
| GBSeq XML | gb | xml |
| INSDSeq XML | gbc | xml |

#### Additional option for db = nuccore and protein
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| Feature table | ft | text |

#### Additional option for db = nuccore
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| GenBank flat file with full sequence (contigs) | gbwithparts | text |
| CDS nucleotide FASTA | fasta_cds_na | text |
| CDS protein FASTA | fasta_cds_aa | text |

#### Additional options for db = protein
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| GenPept flat file | gp | text |
| GBSeq XML | gp | xml |
| INSDSeq XML | gpc | xml |
| Identical Protein XML | ipg | xml |

#### db = pmc
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| XML | null | xml, default |
| MEDLINE | medline | text |

#### db = pubmed
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| XML | null | xml, default |
| MEDLINE | medline | text |
| PMID list | uilist | text |
| Abstract | abstract | text |

#### db = sequences
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| text ASN.1 | null | text, default |
| Accession number(s) | acc | text |
| FASTA | fasta | text |
| SeqID string | seqid | text |

#### db = snp
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| text ASN.1 | null | asn.1, default |
| XML | null | xml |
| Flat file | flt | text |
| FASTA | fasta | text |
| RS Cluster report | rsr | text |
| SS Exemplar list | ssexemplar | text |
| Chromosome report | chr | text |
| Summary | docset | text |
| UID list | uilist | text or xml |

#### db = sra
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| XML | full, default | xml, default |

#### db = taxonomy
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| XML | null | xml, default |
| TaxID list | uilist | text or xml |

#### db = clinvar
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| ClinVar Set | clinvarset | xml, default |
| UID list | uilist | text or xml |

#### db = gtr
| Record Type | &rettype | &retmode |
| ---| ---| ---|
| GTR Test Report | gtracc | xml, default |