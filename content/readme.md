
###  圖片管理規範 (Image Management)

為了保持專案結構整潔並方便維護，請遵循以下圖片存放規則：

#### 1. 文章專用圖片 (Page Bundles) - **最推薦**

針對特定車輛或文章的圖片，請將其與 `.md` 檔案放在同一個資料夾中。

* **路徑範例**：`content/n-gauge/brands/kato/ef210/`
* **結構**：
* `index.md` (文章主體)
* `ef210-side.jpg` (該文章專用圖)


* **優點**：刪除文章時，圖片會一併移除，不會產生孤兒檔案。

#### 2. 全站通用資源 (Global Assets)

如果是首頁按鈕背景、Logo 或多個頁面共用的裝飾圖，請存放在 `static` 目錄。

* **路徑範例**：`static/images/ui/`
* **結構**：
* `comparison-hero.jpg` (首頁大按鈕背景)


* **引用路徑**：在 CSS 或 HTML 中直接使用 `/images/ui/xxx.jpg`。

#### 3. 命名原則 (Naming Convention)

* **全小寫**：避免大小寫造成的讀取錯誤（例如：使用 `kato-ef210.jpg` 而非 `Kato_EF210.JPG`）。
* **無空格**：單字間以連字號 `-` 隔開。
* **有意義的描述**：依照 `品牌-型號-視角.jpg` 命名，方便未來搜尋。

###  型式分頁管理規範

🛠️ 1. 建議的目錄結構
將 comparison 變成一個大類別，裡面按「型號」分資料夾：

content/
└── comparison/
    ├── _index.md             (型式專欄首頁，顯示所有型號列表)
    └── ef210/                (EF210 型號專區)
        ├── _index.md         (設定標題為 "EF210 專欄")
        ├── kato-ef210.md     (KATO 版評測)
        ├── tomix-ef210.md    (TOMIX 版評測)
        └── sanying-ef210.md  (三鶯重工版評測)