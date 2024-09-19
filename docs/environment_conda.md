# **Create a QGIS environment with conda.**

QGIS 環境は anaconda や mamba でも作成する事が出来る。

```
>>> mamba create --name ENV_NAME python=3.x
>>> mamba install qgis --channel conda-forge
```

※ anaconda.org でも QGIS のインストールコマンドが書かれていますが、そのコマンドでインストールすると QGIS のアプリケーションがインストールされないので、上記のコマンドでインストールする必要があります。

> Using QGIS from Conda: https://plugins.qgis.org/planet/tag/conda/