# CMD command
* setlocal enabledelayedexpansion
    設定的值可以直接動態變化

* for
1. for 
    直接做重複執行的動作
2. for /f
    從file分割字串

<code>
for /f "delims=" %%a in (file.txt) do (
  for /f "tokens=1,2" %%b in ("%%a") do (
    echo %%b
    if(%%b)
    echo %%c
  )
)
</code>

    1. delims: 分隔號
    2. tokens: 要使用分割的第幾個


‧ %~I        - 展開 %I 且移除包圍的引號 (")
‧ %~fI       - 展開 %I 為一個完全符合的路徑名稱
‧ %~dI       - 只展開 %I 為磁碟機代號
‧ %~pI       - 只展開 %I 為路徑
‧ %~nI       - 只展開 %I 為檔名
‧ %~xI       - 只展開 %I 為副檔名
‧ %~sI       - 展開的路徑只包含短檔名
‧ %~aI       - 展開 %I 為檔案的檔案屬性
‧ %~tI       - 展開 %I 為檔案的日期/時間
‧ %~zI       - 展開 %I 檔案的長度
‧ %~$PATH:I  - 搜尋所有列在 PATH 環境變數內的目錄且展開 %I 為第一個找到的完全符合檔名。如果沒有定義環境變數名稱或是搜尋找不到檔案，則這個修飾元會展開為空字串。

修飾元可以合併使用以獲得綜合的結果:
‧ %~dpI       - 只展開 %I 為磁碟機代號與路徑
‧ %~nxI       - 只展開 %I 為檔名與副檔名
‧ %~fsI       - 只展開 %I 為含短檔名的完全路徑
‧ %~dp$PATH:i - 為 %I 搜尋所有列在 PATH 環境變數內的目錄且展開第一個找到的項目為磁碟機代號及路徑。
‧ %~ftzaI     - 展開 %I 為像 DIR 一樣的輸出行

* awk

1. awk 'NR>=2{print $1}'
    NR>=2: skip first line
    print $1: print first row

    Example: 
    list the modified files whose paths include cmsm01
    <code>
    git diff development pre-production --name-status | awk '{if($1=='M'){print $2}}' | grep "cmsm01"
    </code>  
