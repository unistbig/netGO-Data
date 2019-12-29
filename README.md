# netGO-Data

This repository contains pre-calculated R object files for demo use.<br>

## netGO ( Calculation ) 

To run netGO, four input data are requird as follows: genes, genesets, network, genesetV. <br>

## Usage table 

### Human (in human directory)

|Data|Genes|Genesets|Network|GenesetV|
|:---:|:---:|:---:|:---:|:---:|
|Breast Tumor|brca.RData|c2gs.RData|networkString.RData networkHumannet.RData|genesetVString1,2.RData genesetVHumannet1,2.RData|
|P53|p53.RData|c2gs.RData|networkString.RData networkHumannet.RData|genesetVString1,2.RData genesetVHumannet1,2.RData|
|Diabetes|dg.RData|cpGenesets.RData|networkString.RData networkHumannet.RData|cpgenesetV1,2.RData|

*dgans.Rdata is standard positive gene-sets for Diabetes*
*brcaans.Rdata is standard positive gene-sets for Breast Tumor*

**or the user can use Breast Tumor data using DownloadExampleData function in netGO (Recommended)** 

### Arabidopsis thalinana

|Data|Genes|Genesets|Network|GenesetV|
|:---:|:---:|:---:|:---:|:---:|
|ShadowResponse|Aragenes.RData|KEGGara.RData|networkAranet.RData|AragenesetV.RData|

### Important

The original genesetV.RData (>25Mb) file was splitted into two to upload to github<br>
So they should be combined using **rbind**. For example,

```r 
load("genesetVString1.RData") # load genesetV1
load("genesetVString2.RData") # load genesetV2
genesetV = rbind(genesetV1,genesetV2)
rm(genesetV1,genesetV2) # for clear memory usage, optional
```

## netGOVis (Visualization)

netGOVis function requires four data as follows : Obj, Genes, Genesets, Network<br>

## Usage table 

|Data|Obj|Genes|Genesets|Network|
|:---:|:---:|:---:|:---:|:---:|
|BreastTumor|brcaresult.RData|brca.RData|c2gs.RData|networkString.RData|
|ShadowResponse|shadowResult.RData|Aragenes.RData|KEGGara.RData|networkAranet.RData|

*Note that pre-calculated brcaresult is built with brca[1:30], so **only brca[1:30] should be used**.*

## Sources of data (version omitted)

### Genes
Human : [BreastTumor](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE3744), [P53](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE35896), [Diabete](https://diagram-consortium.org/index.html)
<br>
Yeast : [ShadowResponse](https://www.inetbio.org/yeastnet/)<br>
### Gene-sets
[mSigDB](http://software.broadinstitute.org/gsea/msigdb/index.jsp), [KEGG](https://www.genome.jp/kegg/pathway.html)
<br>
### Networks
[stringDB](https://string-db.org/), [HumanNet](https://www.inetbio.org/humannet/), [AraNet](https://www.inetbio.org/aranet/), [YeastNet](https://www.inetbio.org/yeastnet/), [MouseNet](https://www.inetbio.org/mousenet/)
<br>

Question / Comment / Suggest : kjh0530@unist.ac.kr, dougnam@unist.ac.kr

Thanks.

