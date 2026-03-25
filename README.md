# 網站維護說明

# 目錄說明
* [/pages](/pages)
首頁、關於我們、出版品
* [/assets/images](/assets/images)
圖片目錄，儘量以子目錄分類圖片
* [/posts](/posts)
最新活動消息
* [/_introduction](/_introduction)
關於讀經
* [/_testimony](/_testimony)
讀經見證
* [/_jewish](/_jewish)
猶太教育
* /_data 網站設定資料
* /example 範例網頁

# 設定
## 選單
[/_data/navigation.yml](/_data/navigation.yml)

## 相關資源
[/_data/external_links.yml](/_data/external_links.yml)
## 出版品
[/_data/books.yml](/_data/books.yml)

## 首頁事工簡介
[/_data/projects.yml](/_data/projects.yml)
## 團隊
[/_data/team.yml](/_data/team.yml)

# 最新活動消息

在新增文章之前，建議先閱讀 [常用 Markdown 語法說明](MARKDOWN.md) 以了解如何撰寫內容。

## 如何新增消息 (使用 GitHub 網頁介面)

請依照以下步驟新增最新的活動消息：

1.  **進入文章目錄**：
    在 GitHub 專案首頁，點擊進入 `_posts` 資料夾。

2.  **建立新檔案**：
    點擊右上角的「新增檔案 (Add file)」按鈕，然後選擇「建立新檔案 (Create new file)」。

3.  **命名檔案**：
    在「命名您的檔案... (Name your file...)」欄位中輸入檔名。
    *   **格式必須為**：`YYYY-MM-DD-文章標題.md`
    *   **範例**：`2024-03-25-春季讀經講座.md`
    *   **注意**：檔名中的日期主要用於系統辨識與預設排序，實際在網頁上顯示的日期則由下方的 `date` 屬性決定。

4.  **設定文章屬性 (Front Matter)**：
    在檔案編輯區的最上方，**必須**包含以下內容（請直接複製貼上並修改）：

    ```yaml
    ---
    layout: post
    title: "這裡是文章標題"
    date: 2024-03-25 00:00:00 +0800
    tags: 活動
    # 分類必須用英文
    categories: [news]
    # 指定較小的圖、寬度 350px (選填)
    post_image: "news/default-image"
    ---
    ```

    *   `title`: 文章顯示的標題。
    *   `date`: **這才是網頁上實際顯示的日期**（格式為 `YYYY-MM-DD HH:MM:SS +0800`）。如果檔名日期與這裡的日期不同，網頁會以這裡的設定為準。
    *   `tags`: 標籤，例如「活動」、「講座」。
    *   `categories`: 分類，固定填寫 `[news]`。
    *   `post_image`: 封面圖片路徑（選填），通常放在 `assets/images/news/` 下。

5.  **撰寫內容**：
    在第二個 `---` 之後，開始撰寫文章內容。您可以使用 Markdown 語法來排版。

    ```markdown
    # 這是大標題

    這裡是內文，可以包含**粗體**或是[連結](https://google.com)。

    ![活動照片](/assets/images/news/photo.jpg)
    ```

6.  **預覽變更**：
    點擊編輯框上方的「預覽 (Preview)」頁籤，確認排版顯示是否正確。

7.  **提交變更 (儲存)**：
    確認無誤後，點擊頁面右上方的「提交變更... (Commit changes...)」按鈕。
    *   在「提交訊息 (Commit message)」欄位簡單說明這次的更動（例如：新增春季讀經講座文章）。
    *   點擊下方的「提交變更 (Commit changes)」按鈕完成發布。

8.  **等待發布與驗證 (Deployment and Verification)**：
    *   **等待發布**：提交變更 (Commit changes) 後，請耐心等待約 3 到 5 分鐘，GitHub 會自動進行網站部署。隨後便可在網站上看到更新後的內容。
    *   **檢查部署狀態**：若更新未如預期出現，可點擊 GitHub 儲存庫頁面右側的「部署 (Deployments)」項目，查看最近一次的部署記錄是否顯示「失敗 (Failure)」。


# 圖片來源
* [unsplash]()
* [大都會藝術博物館](https://www.metmuseum.org/art/collection)

# 技術細節
[DEV.md](DEV.md)
