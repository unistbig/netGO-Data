# netGO-Data

This repository is built for pre-calculated R object files for demo use.
If you want to get information about [netGO](https://github.com/unistbig/netGO),<br> 
Please refer this link.

## for netGO (calculation), <br>

use brca.RData or p53.RData for genes<br>
use c2gs.RData for genesets<br>
use PPIString.RData & genesetVString.RData <br>
or PPIHumannet.RData & genesetVHumannet.RData for PPI and genesetV, **they need to be paired** <br>

this works for human dataset.

Notice that genesetV files are large size, so need to download all zipped file and use after unzip.<br>

**or you can use just DownloadExampleData function in netGO (Recommended)**

## for netGOVis (visualization)
use obj.RData for obj,<br>
use Top 10 gene of brca.RData ( ``` brca[1:10] ``` ) for genes, <br>
use c2gs.RData for genesets,<br>
use PPIString.RData for PPI.<br>

### Other species 
PPI for other 3 species ( Arabidopsis, Mouse, Yeast ) are prepared <br>
also user can use prepared gene-sets from [KEGG](https://www.genome.jp/kegg/)<br>
and pre-calculated interaction variable. 

question / comment : kjh0530@unist.ac.kr

thanks
