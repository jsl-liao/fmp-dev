### 從 FileMaker 建立 menuTree 一個可以折疊的樹狀清單

1. 可以選擇建立 url list 或者 button list
1. url list 僅做為 url 清單(如果menuTree 要當網頁管理: 選擇 url )
1. 在 button list(如果menuTree 要當腳本選擇器: 選擇 button), FileMaker 可以接收從 web viewer 傳回點擊取得的 node id, 進行後續的處理; 在資料庫中以 custom dialog 作演示
1. 接收 menuTree 傳回參數的腳本名稱: getFromMenuTree
> #### 簡要內容如下
> ---
>> Set Error Capture [ On ] 
>> Allow User Abort [ Off ] 
>> Set Variable [ $nodeId ; Value: Get(ScriptParameter) ] // 接收 menuTree 傳回參數
>> if ( $nodeId = "value_1" ; do something ; do something else )
>
>
6. 在 menuTree 視窗可以測試實際成果, 檢視完成的 html code
1. menuTree 是樹狀結構, 須由上而下逐級填寫.
1. 允許四個層級內的 menu.
1. 層級編號允許兩個字元英數字, 自動轉為大寫.
1. 列表中的編號為個位數號碼, 青色表示: 兩個字元, 第一個字元不是 0
1. 資料結構由節點編號構成.
1. 名稱和網址是連動的, 相同節點編號(nodeId)的名稱和網址是共用的; 在某一筆更動其值, 其他紀錄中引用相同編號的名稱和網址也被更改.
1. 執行產生 menuTree 命令, 產生新 menuTree html(青色表示即將產生的 menuTree 的形式).
1. menuTree 命令依 found set 是產生 html, 依據查詢的結果不同, 產生不同的 menuTree; 在 node id 編號加以區分
1. url 如果未輸入資料, 自動以 # 置入.
1. FileMaker版本: V19.1 以上; 在 web viewer 中以 FileMaker.PerformScriptWithOption 傳出參數
1. refJson 是參考的 json data; 考慮到執行效率, menuTree 與 refJson 未自動同步處理(guest account 看不到)
1. 977筆資料在 mbp 2013 上產生 menuTree 約 13 秒, 100筆資料少於 1 秒.
1. 目前建立的清單是依據 FileMaker help 的左側清單列的內容建立的; 這是為了可以檢查資料庫是否可以產生正確的數據.
1. editable account: fm3275, password:fm3275
