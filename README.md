# 水費異常處理工具

純前端小工具，所有資料只在瀏覽器內處理，不會上傳。

## 功能
1. **異常報表處理**：匯入 WBZF3650／WBZF3280 PDF，產出異常處理表格（可貼到 Excel）
2. **差額解釋產出**：貼上或匯入 Excel，產出差額說明文字
3. **手續費明細（WA2900）**：匯入代收、代繳兩份 WA2900 PDF，產出含公式的手續費明細（`=12110+125947+718+636`），可複製貼進 Excel

PDF 皆可直接拖曳到頁面上的匯入區塊。

## 專案結構
```
index.html                 主程式（HTML + CSS + JS）
libs/pdf.min.js            pdf.js 3.11.174（讀 PDF）
libs/pdf.worker.min.js     pdf.js 的 worker（與上面成對，版本需一致）
libs/xlsx.full.min.js      SheetJS 0.18.5（讀 Excel）
```

## 使用
- 本機：直接雙擊 `index.html`（不需連網）
- GitHub Pages：Settings → Pages → Branch 選 `main` / `(root)` → Save，約一分鐘後取得網址

## 注意
- **請勿把實際的 WA2900／WBZF PDF 或含水號的 Excel 提交到 repo**（repo 若為公開，內容人人可見）。
- 升級 pdf.js 時，`pdf.min.js` 與 `pdf.worker.min.js` 必須同版本一起換。

## 授權
- pdf.js：Apache-2.0（Mozilla）
- SheetJS Community Edition：Apache-2.0
