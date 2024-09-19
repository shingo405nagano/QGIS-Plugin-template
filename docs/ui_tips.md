# **UI Tips**

## **1. FileWidget で目的のフォーマットだけに絞り込む**
```
>>> mQgsFileWidget.setFilter("GeoTiff (*.tif *.tiff *.TIF *.TIFF);;")
```
<br>

## **2. LayerComboBox で目的のデータタイプだけに絞り込む**

```
>>> from qgis.core import QgsMapLayerProxyModel
>>> mMapLayerComboBox.setFilters(QgsMapLayerProxyModel.RasterLayer)
```
<br>