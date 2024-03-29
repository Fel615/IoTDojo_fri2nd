
# Location Database README

このドキュメントは、`location.db` SQLiteデータベースに関する説明です。このデータベースには、ポスト、ルート、センサー、壊れたesp32に関する情報が含まれています。

## テーブル

### 1. post

| カラム名   | データ型        | 説明                                |
|------------|-----------------|-------------------------------------|
| id         | INTEGER        | 主キー                              |
| gps        | INTEGER        | GPS座標                             |
| num_gps    | INTEGER        | GPS座標の数                         |
| ins        | VARCHAR(100)   | 指示                               |
| esp_name   | VARCHAR(100)   | ESP名                               |

サンプルデータ:
```
1, '35.67181545147268,139.69172210148648', '35.67243165493962, 139.69149625341186', 'office', 'office'
2, '35.673500896630685, 139.69338567952164', '35.67373465848754, 139.6929446511895', 'node', 'node1'
...
```

### 2. route

| カラム名 | データ型   | 説明           |
|----------|------------|----------------|
| id       | TEXT       | ルートID      |
| route    | TEXT       | ルートの順序  |

サンプルデータ:
```
'1', '05_03_01_2'
'2', '09_07_03_01_3'
...
```

### 3. sensor

| カラム名 | データ型   | 説明          |
|----------|------------|--------------|
| id       | TEXT       | センサーID   |
| val      | TEXT       | センサーの値 |
| date     | TEXT       | 読み取り日   |
| time     | TEXT       | 読み取り時間 |

サンプルデータ:
```
'2', '131', '20230710', '150940'
'3', '408', '20230710', '150950'
...
```
### 4. breakesp

| カラム名 | データ型   | 説明          |
|----------|------------|--------------|
| id       | TEXT       | センサーID   |


サンプルデータ:
```
'2'
'3'
...
```
