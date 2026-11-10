# 11/21 生日驚喜網頁

純 HTML、CSS 與原生 JavaScript，不使用前端框架，不需要 npm 或建置指令。房間背景已嵌入主頁；Mac 是 CSS 3D 元件，會沿鉸鏈連續慢慢開蓋，不是切換筆電圖片。音樂由 Web Audio 即時合成。

## 發布到 GitHub Pages

1. 開啟本儲存庫的 [Settings → Pages](https://github.com/stu310101-arch/birthday/settings/pages)。
2. 在 Build and deployment 中，把 Source 設為 **Deploy from a branch**。
3. Branch 選 **main**，資料夾選 **/ (root)**，按 **Save**。
4. 等 GitHub 顯示發布成功後，開啟 [生日網頁](https://stu310101-arch.github.io/birthday/)。

正式網址：`https://stu310101-arch.github.io/birthday/`

`.nojekyll` 已放在根目錄。檔案名稱必須保留為 `index.html`。不要把整個 ZIP 檔直接當網站上傳，也不要把網頁放進額外一層資料夾。

## 直接從網站寄信：首次啟用

回覆透過 FormSubmit AJAX 送往 **stu310101@shsh.tw**，不會開啟使用者的郵件程式。GitHub Pages 提供靜態網頁；實際郵件由 FormSubmit 處理。

1. 網站發布成功後，開啟 [寄信啟用與測試頁](https://stu310101-arch.github.io/birthday/setup.html)。
2. 按「寄出啟用／測試信」。這會實際提交一封明確標示為測試的信，不是壽星的回覆。
3. 到 **stu310101@shsh.tw** 收取 FormSubmit 的首次啟用信，按 **Activate Form**。也請查看垃圾郵件。
4. 回到測試頁再寄一次，核對信箱收到的測試編號。
5. 再由生日主頁送一段測試回覆，確認到信。完成後才分享主頁給壽星。

**服務接受請求，不等於已確認收件匣到信。** 截至本版製作完成，前端寄信成功、失敗、待啟用的分支是以模擬回應測試，沒有代收件人點啟用信，也沒有完成真實到信驗收。

主頁與測試頁已使用同一個 `_url`：`https://stu310101-arch.github.io/birthday/`。若換網域或儲存庫名稱，請同步修改兩處來源設定並重新驗收。請用正式 HTTPS 網址操作，不要把雙擊本機檔案當成正式部署驗收。

測試頁沒有在主頁提供入口，但 **setup.html 仍是公開網頁**。測試完成後可以刪除它，不影響主頁功能。

## 保留的互動與文字

- 首頁：`11/21屬於你的特別日子!!`、`生日快樂 陳巧恩同學`。
- Mac 預設以 3.8 秒連續開蓋，之後顯示聊天。
- 依序收到「1」「2」「3」，尚未收完時不能回覆，也不能提前關閉聊天。
- 收完後解鎖回覆與右上角叉叉，不回覆也能進入蛋糕桌面；未送出的草稿會保留。
- 巧克力蛋糕與 18 蠟燭；點擊吹熄後播放 138 BPM 輕快生日旋律。
- 最後祝福：`願我們在頂峰相見`。
- 已移除指定的舊標誌、介紹與提示，以及 mailto／複製回覆備援。

## 日後修改訊息

在 `index.html` 搜尋 `const CONFIG`，修改 `messages` 陣列。目前為 `['1', '2', '3']`。不要改動下方的動畫與寄信程式。音樂需使用者首次點擊後開始；右上角音樂按鈕可以切換。

## 驗收與隱私

已測試桌面 1440×900、手機 390×844 的慢慢開蓋、訊息順序、輸入鎖定、錯誤時保留回覆、無回覆也能關閉、草稿保留、吹熄蠟燭及音樂切換。寄信測試採模擬回應，沒有自動寄出信件。

網頁與儲存庫是公開的，寄信地址也會出現在原始碼中。不要放入密碼、SMTP 憑證或私密 API 金鑰。回覆會經由第三方 FormSubmit 處理。頁面有 `noindex,nofollow`，但這不是密碼保護，也不能保證完全不被搜尋引擎索引。

## 官方參考

- [GitHub Pages 發布來源設定](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
- [FormSubmit 首次啟用與來源網址](https://formsubmit.co/help)
- [FormSubmit AJAX](https://formsubmit.co/ajax-documentation)
