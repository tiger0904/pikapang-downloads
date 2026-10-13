# PIKAPANG

PIKAPANG 是 Windows 商業卡密版工具，提供遊戲輔助、CAPTCHA 偵測與處理、AutoReply 自動回覆，以及受簽章保護的 GitHub 自動更新。

目前最新公開測試版：**PIKAPANG 2.1.0 Beta 3**

> Beta 3 的技術更新版本為 `2.1.1`，用於讓既有 `2.1.0` Client 正確判定為新版。這是公開測試版，不代表 Stable 正式版。

## 功能介紹

目前 Commercial 版本包含下列已在程式與自動化測試中實作的能力：

- 遊戲輔助功能與受授權保護的主程式流程
- CAPTCHA 偵測、圖片擷取、排序、Provider 處理、輸入讀回與 post-check
- AutoReply 自動回覆與重複事件、自身訊息排除
- AI 回覆與 TXT fallback 模式
- GitHub HTTPS 自動更新
- 更新進度視窗，顯示下載進度、速度、ETA 與交易階段
- 更新完成後自動重新啟動，並在交易完成後關閉進度視窗
- 更新檔案驗證、失敗保護與回滾

部分功能仍需真人環境驗收，請以實際測試結果為準。

## 下載最新版本

- [GitHub Releases](https://github.com/tiger0904/pikapang-downloads/releases)
- [PIKAPANG 2.1.0 Beta 3](https://github.com/tiger0904/pikapang-downloads/releases/tag/v2.1.0-beta.3)

請只從官方 GitHub Releases 下載 Commercial ZIP。公開 Release 不包含 Internal 版本、原始碼、私鑰或測試憑證。

## 使用需求

- Windows 環境
- 有效卡密授權
- 首次啟動需完成授權
- 檢查與下載更新時需要網路連線
- 請從官方 GitHub Releases 取得安裝檔

本專案目前沒有足夠的跨版本硬體或最低 Windows 版本驗證資料，因此不額外宣稱最低系統規格。

## 安裝與啟動

1. 從官方 Releases 下載 Commercial ZIP。
2. 將 ZIP 解壓縮至獨立的安裝目錄。
3. 啟動 `pikapang.exe`。
4. 依畫面完成有效卡密授權。

請保留同一安裝目錄中的必要更新資源，不要將檔案與 Internal 開發版本混用。

## 自動更新

1. 程式檢查 GitHub Beta Release。
2. 使用者確認更新。
3. 顯示下載進度、速度與 ETA；若伺服器沒有提供總大小，進度會保持不確定。
4. 驗證 Manifest 簽章、ZIP 大小與 SHA256。
5. 等待主程式正常退出後安裝更新。
6. 重新啟動並執行 Health Check。
7. 交易成功後自動關閉更新進度視窗；失敗時保留舊版本或回滾。

## Beta 測試注意事項

- 目前為公開測試版，可能仍有尚未發現的問題。
- AutoReply、CAPTCHA 與跨機授權仍在收集真人測試結果。
- Beta 不代表 Stable 正式版，也不代表所有功能已完成真人驗收。
- 遇到異常時，請先停止相關功能並保留安全診斷資訊。
- 請勿公開卡密、Token、私鑰、DPAPI 內容、聊天隱私或其他敏感資料。

## 問題回報

此 Public Repository 已啟用 GitHub Issues：

[提交問題回報](https://github.com/tiger0904/pikapang-downloads/issues)

請盡量提供：

- 程式版本
- Windows 版本
- 發生問題的功能
- 重現步驟
- 預期結果
- 實際結果
- 經安全處理後的錯誤紀錄

回報前請移除卡密、Token、私鑰、聊天內容及其他個人資料。

## 版本紀錄

- **v2.1.0-beta.3**：公開 Beta 3；包含 GitHub 自動更新、進度視窗、更新後自動重啟與完成後關閉視窗。
- **v2.1.0-beta.2**：前一個公開 Beta，保留歷史下載與驗收記錄。

Stable 版本尚未發布。