# QA Notes

AI 問答與筆記的 Markdown 集散地，透過 GitHub Pages 渲染成可瀏覽的網站。

## 網站

啟用後網址為： https://yatinisgood.github.io/QA/

## 使用方式

1. 直接在 repo 根目錄新增 `.md` 檔即可（檔名可用中文）。
2. push 到 `main` 後，GitHub Action 會自動掃描並更新 `files.json`。
3. 網站左側選單會列出所有 md；點選檔案後，該檔的 `##` 標題會展開成子選單，點擊即可跳到對應段落。

## 首次啟用 GitHub Pages

Repo → **Settings** → **Pages** → Source 選 **Deploy from a branch**，
Branch 選 `main` / `(root)`，儲存即可。

## 檔案結構

| 檔案 | 用途 |
|------|------|
| `index.html` | 單頁閱讀器（marked.js 渲染、側邊選單、搜尋、RWD） |
| `files.json` | md 檔清單，由 Action 自動產生（勿手動維護） |
| `.github/workflows/build-manifest.yml` | push 時自動重建 `files.json` |

## 本機預覽

```bash
python -m http.server 8000
# 開瀏覽器 http://localhost:8000
```
