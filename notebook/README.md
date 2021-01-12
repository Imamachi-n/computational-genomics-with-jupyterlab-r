# 事前準備

## 9. ChIP-seq analysis

事前に、以下の R/BioConductor パッケージを `conda` コマンド経由でインストールする。

```zsh
conda install -c bioconda bioconductor-genomeinfodb
conda install -c bioconda bioconductor-genomicranges
conda install -c bioconda bioconductor-genomicalignments
conda install -c bioconda bioconductor-complexheatmap
conda install -c conda-forge r-circlize
conda install -c bioconda bioconductor-rtracklayer
conda install -c bioconda bioconductor-gviz
conda install -c conda-forge r-ggplot2
conda install -c bioconda bioconductor-bsgenome.hsapiens.ucsc.hg38
conda install -c conda-forge r-tidyr
conda install -c bioconda bioconductor-annotationhub
conda install -c bioconda bioconductor-genomicfeatures
conda install -c bioconda bioconductor-normr
conda install -c bioconda bioconductor-motifdb

conda install -c bioconda bioconductor-dirichletmultinomial

conda install -c bioconda bioconductor-tfbstools
conda install -c bioconda bioconductor-jaspar2018
```

もしくは、R console 経由でインストールする。

```r
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("GenomeInfoDb")
BiocManager::install("GenomicRanges")
BiocManager::install("GenomicAlignments")
BiocManager::install("ComplexHeatmap")
install.packages("r-circlize")
BiocManager::install("rtracklayer")
BiocManager::install("Gviz")
install.packages("ggplot2")
BiocManager::install("BSgenome.Hsapiens.UCSC.hg38")
install.packages("tidyr")
BiocManager::install("AnnotationHub")
BiocManager::install("GenomicFeatures")
BiocManager::install("normr")
BiocManager::install("MotifDb")
BiocManager::install("TFBSTools")
BiocManager::install("JASPAR2018")
```

## トラブルシューティング

### ERROR: configuration failed for package ‘Cairo’

`ComplexHeatmap` ライブラリをインストールする際に、`Cairo` ライブラリがインストールできない場合、以下のコマンドをターミナルで実行する(MacOS の場合)。

自身のパソコンに `cairo` 自体がインストールされていないことが原因かもしれない。

```zsh
brew update
brew install cairo
```

これでも解決しない場合、以下も追加で実行。

```zsh
brew install pkg-config
```

zsh を使っている場合、`.zshrc` ファイルに以下を追加。

```
export PKG_CONFIG_PATH=/opt/X11/lib/pkgconfig
```

リロード。

```zsh
source ~/.zshrc
```

### ERROR: dependency ‘DirichletMultinomial’ is not available for package ‘TFBSTools’

`TFBSTools` ライブラリをインストールする際に、`DirichletMultinomial` ライブラリがインストールできない場合、以下のコマンドをターミナルで実行する(MacOS の場合)。

```zsh
brew install gsl
```
