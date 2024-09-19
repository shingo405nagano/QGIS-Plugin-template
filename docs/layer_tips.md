# **Layer**

## **1. Layer名の取得**
```
>>> print(lyr)
<QgsRasterLayer: 'OpenStreetMap' (wms)>

>>> print(lyr.name())
OpenStreetMap
```
<br>

## **2. Layer source の取得**
```
>>> lyr.source()
'crs=EPSG:3857&format&type=xyz&url=https://tile.openstreetmap.org/%7Bz%7D/%7Bx%7D/%7By%7D.png&zmax=19&zmin=0'

>>> lyr.source()
'D:/Repositories/ProcessingRaster/datasets/DEM638.tif'
```
<br>

## **3. Layer type の取得**
```
>>> lyr.type()
<LayerType.Raster: 1>
```
<br>

## **4. Provider の取得**
```
>>> lyr.providerType()
```
<br>

## **5. Layerの中から任意のProbiderのデータだけ取得する**
これは例えば Dialog の `QgsMapLayerComboBox` を使用する際にレイヤーから Tiff などの RasterLayer だけをコンボボックスに表示させる事が出来る。
```
>>> def lyr_filter(provider_type: str):
>>>     lyrs = iface.mapCanvas().layers()
>>>     filtered = []
>>>     for lyr in lyrs:
>>>         if lyr.providerType() == provider_type:
>>>             filtered.append(lyr)
>>>     return filtered
```
<br>

## **6. field 関連のデータ取得**

```
# Field の取得
>>> lyr.field()

# Alias の取得
>>> lyr.alias()

# データ型を文字列で取得する
>>> lyr.typeName()
```