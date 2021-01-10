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
```

## トラブルシューティング

### ERROR: configuration failed for package ‘Cairo’

`ComplexHeatmap` ライブラリをインストールする際に、`Cairo` ライブラリがインストールできない場合、以下のコマンドをターミナルで実行する(MacOS の場合)。

自身のパソコンに `cairo` 自体がインストールされていないことが原因かもしれない。

```zsh
brew update
brew install cairo
```
