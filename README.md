# Dora 的學習與工作筆記

使用 GitHub Pages 支援的 Jekyll／Minima 主題，不另寫發文後台。

## 目前狀態

儲存庫已建立：`DoraC7/dora-notes`。
網站預定網址：`https://dorac7.github.io/dora-notes/`。首次發布須啟用 GitHub Pages 並等待建置完成；原始碼上傳不等於網站已上線。

## 發表文章

1. 在 HackMD 寫文章，完成後匯出 Markdown；不會自動同步。

   在文章最前方加入：

   ```yaml
   ---
   layout: post
   title: "文章標題"
   categories: [學習]
   ---
   ```
2. 把 `_drafts/first-note.md` 的 YAML 開頭放在文章最前面，改標題及分類。
3. 將完成的文章存成 `_posts/YYYY-MM-DD-english-slug.md`。日期使用發表日。
4. 圖片放到 `assets/images/`；圖片路徑用 `{{ '/assets/images/檔名.png' | relative_url }}`。
5. 提交並推送後，由 GitHub Pages 建置發布。

分類可用 `[學習]` 或 `[工作]`；草稿留在 `_drafts/` 不會列為正式文章，且此目錄已加入 Git 忽略清單，不會隨一般提交上傳。私人草稿建議留在 HackMD 私人筆記／本機。
文章模板不會公開上傳；新文章可先在 HackMD 撰寫，再依上方 YAML 範例設定。

## 首次上線

1. 使用獨立儲存庫 `DoraC7/dora-notes`，不要放進遊戲專案。
2. 檢查 `_config.yml` 的 `url`／`baseurl` 與實際儲存庫一致。
3. 上傳檔案，GitHub Settings → Pages → Deploy from a branch → main / root。
4. 等待 GitHub Pages 建置成功，再檢查首頁、文章、手機版及連結。

## 本機預覽

需要 Ruby 和 Bundler：`bundle install`，然後 `bundle exec jekyll serve`。
目前工作環境沒有 Ruby／Jekyll，尚未執行完整建置或瀏覽器驗證。

## 主題

現成 Minima 主題：https://github.com/jekyll/minima
此專案只用其設定及官方支援的樣式覆寫，沒有複製主題原始碼。
