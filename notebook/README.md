# 事前準備

## 9. ChIP-seq analysis

事前に、以下の BioConductor パッケージをインストールする。

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
```

## トラブルシューティング

### ERROR: configuration failed for package ‘Cairo’

`ComplexHeatmap` ライブラリをインストールする際に、`Cairo` ライブラリがインストールできない場合、以下のコマンドをターミナルで実行する(MacOS の場合)。

自身のパソコンに `cairo` 自体がインストールされていないことが原因かもしれない。

```zsh
brew update
brew install cairo
```

これでも解決しない場合、以下も追加。

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
