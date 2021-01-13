# computational-genomics-with-jupyterlab-r

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Imamachi-n/computational-genomics-with-jupyterlab-r/main?filepath=notebook%2F9_ChIP-seq_analysis_QC.ipynb)

[Computational Genomics with R](https://compgenomr.github.io/book/) を Jupyter Notebook (WebIDE として JupyterLab を使用) で記述したサンプル集です。

## 🏗 MyBinder を利用した JupyterLab (WebIDE)の起動

以下の URL にアクセスしてください。  
<https://mybinder.org/v2/gh/Imamachi-n/computational-genomics-with-jupyterlab-r/main?filepath=notebook%2F9_ChIP-seq_analysis_QC.ipynb>

ローカルで環境構築することなく、Web ブラウザ上で JupyterLab を起動することができます。  
（外部のデータベースにアクセス & データをキャッシュする処理を実行している箇所は、MyBinder ではエラーとなるので注意 🚧）

## 🛠 環境構築（ローカル実行する場合）

1. [anaconda](https://www.anaconda.com/products/individual#Downloads) をインストールする。
1. 以下のコマンドを実行（[参考](https://jupyter.org/install)）。

   ```zsh
   conda install -c conda-forge jupyterlab
   ```

1. [IRkernel](https://irkernel.github.io/installation/#binary-panel) をインストールする。

   ```zsh
   R
   ```

   ```r
   # 1/3) Installing via CRAN
   install.packages('IRkernel')

   # 2/3) Making the kernel available to Jupyter
   IRkernel::installspec()
   ```

   ```zsh
   # 3/3) Make useful shortcuts available
   jupyter labextension install @techrah/text-shortcuts
   ```

1. JupyterLab を起動する。

   ```zsh
   jupyter-lab
   ```
