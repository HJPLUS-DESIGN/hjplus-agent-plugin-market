# HJPLUS.DESIGN Agent Plugin Market

HJPLUS Desktop Agent 的官方外掛市集 registry 與散佈來源。

## 這是什麼
宿主 app 讀取本 repo 的 `registry.json` 取得可安裝外掛清單，並從各外掛的 GitHub Release 下載打包好的 zip 安裝。

- 官方策展：僅收錄 HJPLUS 自家外掛。
- 只放公開版（免費 edition）；付費版不在此散佈。
- 平台：先 Windows。

## 結構
- `registry.json` — 外掛索引（宿主讀這份）
- Releases — 各外掛的 dist zip（asset），tag 形如 `<plugin-id>-v<version>`

## registry.json 欄位
| 欄位 | 說明 |
|---|---|
| id | 外掛 id（= 安裝目錄名）|
| name / description / icon / author | 顯示用 |
| version | 該外掛版本 |
| min_app_version | 低於此宿主版本不顯示 |
| edition | 一律 public |
| download_url | 對應 Release asset 的 zip 網址 |
| sha256 | zip 校驗碼 |
| size | zip 位元組數 |

計畫文件見宿主 repo `docs/dev/plan-plugin-marketplace.md`。
