# **CRS modules**

## **1. EPSG を取得**
```
>>> epsg = lyr.crs().authid()

"EPSG:4326"

# 数字だけ取り出したい
>>> epsg = lyr.crs().authid().split(":")[1]

4326
```
<br>

## **2. WKT-CRS を取得**
```
>>> wkt_crs = lyr.crs().toWkt()
```
<br>

## **3. Proj4 を取得**
```
>>> proj4 = lyr.crs().toProj4()
```
<br>


## **4. 楕円体の頭字語 を取得**
```
>>> ellipsoid_epsg = lyr.crs().ellipsoidAcronym()
```
<br>

## **5. CRS の説明を取得**
```
>>> crs_description = lyr.crs().description()

'JGD2011 / Japan Plane Rectangular CS IV'
```
<br>

## **6. 座標系の示す範囲を WKT で取得**
使いどころは無さそうだが、記事を書く時に使用するかも ...
```
>>> poly_wkt = lyr.crs().bounds().asWktPolygon()
```
<br>