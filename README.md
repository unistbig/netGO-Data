# netGO-Data

This repository is built for pre-calculated R object files for demo use.<br>
If you want to get information about netGO,<br> 
Please refer this link [netGO](https://github.com/unistbig/netGO).<br>

## netGO ( Calculation ) 

To run netGO, 4 data are needed. <br>
Genes, Genesets, Network, GenesetV. <br>

## Usage table 

### Human (in human directory)

|Data|Genes|Genesets|Network|GenesetV|
|:---:|:---:|:---:|:---:|:---:|
|Breast Tumor|brca.RData|c2gs.RData|networkString.RData networkHumannet.RData|genesetVString1,2.RData genesetVHumannet1,2.RData|
|P53|p53.RData|c2gs.RData|networkString.RData networkHumannet.RData|genesetVString1,2.RData genesetVHumannet1,2.RData|
|Diabete|dg.RData|cpGenesets.RData|networkString.RData networkHumannet.RData|cpgenesetV1,2.RData|

**or you can use Breast Tumor data with DownloadExampleData function in netGO (Recommended)** 

### Arabidopsis

|Data|Genes|Genesets|Network|GenesetV|
|:---:|:---:|:---:|:---:|:---:|
|ShadowResponse|Aragenes.RData|KEGGara.RData|networkAranet.RData|AragenesetV.RData|

### Important

Original genesetV.RData file is large enough (>25Mb), so we splitted to upload in github. <br>
So you must **rbind** them before use, for example .

```r 
load("genesetVString1.RData") # load genesetV1
load("genesetVString2.RData") # load genesetV2
genesetV = rbind(genesetV1,genesetV2)
rm(genesetV1,genesetV2) # for clear memory usage, optional
```

## netGOVis (Visualization)

To run netGOVis, 4 data are needed. <br>
Obj, Genes, Genesets, Network. <br>

## Usage table 

|Data|Obj|Genes|Genesets|Network|
|:---:|:---:|:---:|:---:|:---:|
|BreastTumor|brcaresult.RData|brca.RData|c2gs.RData|networkString.RData|
|ShadowResponse|shadowResult.RData|Aragenes.RData|KEGGara.RData|networkAranet.RData|

*notice that pre-calculated brcaresult is built with brca[1:30], so **you must use brca[1:30]** not all brca genes.*

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

Question / Comment / Suggest : kjh0530@unist.ac.kr

Thanks.

