dwindling value list
1. onObjectModify: 從 object 取得的值是在執行 script 前的值; 所以由 script 產生的字串"選擇茶點" 只會是提示, 
在計算的過程中, 完全不會被引用
;如果需要, 也可以加上樣式
2. 選單中的 -清除- 是在計算式中加入的, 不在原始的清單中; 當選擇 -清除- , 則會清除已選的項目
3. 利用 filterValues 達成
1.被選上的 item 組成的清單是經過排序後, 咖啡>紅茶>綠茶>其
2.不同的類別加上了顏色樣式
3.清除計算式中 uniqueValues 所產生的空
4. FileMaker 的字串函數在處理 values 有些會產生 trailing returen; 只要看到函數名稱中出現負數 values, 就是會產生 trailing returen
