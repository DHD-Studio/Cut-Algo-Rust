# 鋁料切割

公司統一進貨 `5800mm` 長的鋁料，
生產產品需要切割成長度介於 `0~5800mm` 不等，
每次切割會消耗掉 `2mm` 長的鋁料，
要求的長度中會出現最多一位小數，
計算浪費鋁料最少的方法。

一次只會計算一種形狀的鋁料所以只須考慮長度問題。

## 計算方法

1. 先使用剩於鋁料之中最長的(貪心法)

對於實作應該也比較容易，
目前的 `v1` 就是使用貪心法，
簡單來說先拿最長的，
再來只要不超出範圍都選擇最長條的鋁料，
直到剩下的料無法使用(比剩餘鋁料中最短的短)。

2. 動態規劃

對於實作來說難度會提高不少，
但是比起貪心法來說計算結果更為精準。

3. AE-QTS

使用最佳化演算法，
不保證最佳解但是可以快速得到一個不錯的解。

## 使用方法

在 `input.txt` 內輸入

```
數量1  長度1
數量2  長度2
```

輸入好以後存檔並執行 `cut.exe`，
會生成一個檔案叫做 `output.txt`。

每一行的 `ans =` 後面會寫著每一支 `5800mm` 的料可以切成哪幾部分。
並且會記錄下每一支所浪費掉的鋁料長度。
