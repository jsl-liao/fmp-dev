## 目的:
1. 管理在開發 app 時所寫的檔案
2. 將常用 FileMaker App 集中管理
3. 小規模的檔案管理器
4. 學習 BaseElements-Plugin

## 操作: 
抓取指定資料夾內的檔案和資料夾路徑, 產生可折疊 menuTree 的 html 碼, 在 web viewer 點擊內容, 以系統指定的應用程式打開檔案

* 開發環境: OSX 15.7, FileMaker 19.4.2
* 必需條件: FileMaker 19.1以上, SF symbol, BaseElements Plugin（建議 4.2以上)

* 路徑限制 600 條以內, 路徑層級 7 層以內, 超過 7 層, 會發生對齊不正確
* 􀊯 取得指定的路徑取得路徑與檔案資訊, 並製作 menuTree, 存檔
* 􀻵 在 web viewer 顯示存檔的資料
* 在 web viewer 點擊項目, 可以以系統內定的應用程式打開檔案或資料夾(目錄)
* 已經測試檔案類別: fmp12, html, css, js, png, numbers, pages, zip, rtf, alias 都可以系統指定的應用程式打開檔案

## BaseElements Plugin 的資訊: 

* 首頁: https://docs.baseelementsplugin.com/
* 下載: https://docs.baseelementsplugin.com/article/522-downloads
* 如何安裝: https://docs.baseelementsplugin.com/article/558-how-to-install-the-baseelements-plugin
* 版本資訊: https://github.com/GoyaPtyLtd/BaseElements-Plugin/blob/master/CHANGE_LOG

> 請以你的電腦重新抓取資料, 現有demo的資料不在你的電腦上, 路徑不對, 無法開啟
