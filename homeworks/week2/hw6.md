``` js
function isValid(arr) {
  for(var i=0; i<arr.length; i++) {
    if (arr[i] <= 0) return 'invalid'
  }
  for(var i=2; i<arr.length; i++) {
    if (arr[i] !== arr[i-1] + arr[i-2]) return 'invalid'
  }
  return 'valid'
}

isValid([3, 5, 8, 13, 22, 35])
```

## 執行流程
1. 執行第 11 行，呼叫 isValid 函式，傳入陣列 [3, 5, 8, 13, 22, 35]。
2. 執行第 2 行，設定變數 i 為 0。
3. 執行第 2 行，判斷 i 是否小於 arr 的陣列長度 (6)，是，繼續執行，進入迴圈。
4. 執行第 3 行，如果陣列的 (i+1) 位數的數字 (arr[i])，小於等於 0，回傳 'invalid'；如果大於 0 則繼續執行。
5. 執行第 2 行，i 加 1。
6. 重複 3 ~ 5 步驟，直到 6 次迴圈結束。
7. 執行第 5 行，設定變數 i 為 2。
8. 執行第 5 行，判斷 i 是否小於 arr 的陣列長度 (6)，是，繼續執行，進入迴圈。
9. 執行第 6 行，如果陣列的 (i+1) 位數的數字 (arr[i])，不等於「陣列的 (i) 位數的數字 (arr[i-1])」 以及「陣列的 (i-1) 位數的數字 (arr[i-2])」的總和，回傳 'invalid'；如果是，則繼續執行。
10. 執行第 5 行，i 加 1。
11. 重複 8 ~ 10 步驟，直到 3 次迴圈的第 9 步驟不符合條件，回傳 'invalid'。
12. 結束程式。