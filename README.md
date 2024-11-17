# Day 7 - 嵌套式路由、useRouter & useRoute 題目

請 clone 這一份模板，將 `/pages/room.vue` 改為嵌套式路由，並實作房型列表與房型詳細頁面（不包含動態路由):

- 房型列表頁面的 URL 需對應 `/room/`，在此頁面使用 ES6 Fetch 或 axios 串接 [前台房型 API](https://nuxr3.zeabur.app/swagger/#/Rooms%20-%20%E6%88%BF%E5%9E%8B) ，將資料寫入 `roomList` 變數 ，並在模板的 v-for 使用 roomList 渲染資料。
- 承上，模板的 HTML 、CSS 已有在 `/pages/room.vue` 中提供，需將其移至房型列表頁面並補上 API 串接的 JavaScript 。
- 房型詳細頁面的 URL 需對應 `/room/_id` ，在此頁顯示 “房型詳細頁面” h2 標題。
- 房型列表頁面的列表渲染之後，經點擊可以換頁至 `/room/_id` 。

> 需注意 : `/room/_id` 的 `/_id` 是靜態路由，非動態路由，請建立名稱為 `_id.vue` 的檔案。

- 在房型詳細頁面中提供一個「回上一頁」的按鈕，點擊後可以使用 router 方法返回 `/room/` 的房型列表頁面。
- 確保房型頁面的巢狀路由內容能正確顯示。

## 安裝

以下將會引導你如何安裝此專案到你的電腦上。

Node.js 版本建議為：`18.0.0` 以上

### 取得專案

```bash
git clone -b day7-nested-router  https://github.com/jasonlu0525/nuxt3-live-question.git day7-nested-router-question
```

### 移動到專案內

```bash
cd  day7-nested-router-question
```

### 安裝套件

```bash
npm install
```

### 運行專案

```bash
npm run dev
```

### 開啟專案

在瀏覽器網址列輸入以下即可看到畫面

```bash
http://localhost:3000/
```

# Day 8 - 動態路由與 404 錯誤頁面處理 題目

請 clone 這一份模板，接續 Day7 嵌套式路由的問題，實作房型詳細頁面的動態路由 :

- 將 `pages/room/_id.vue` 調整成房型內頁的動態路由。
- 在 `pages/room/index.vue` 的房型列表中，點擊房型後能夠進入房型內頁。進入房型內頁後，透過動態路由的網址參數 [串接 `/api/v1/rooms/{id}` 這支 API](https://nuxr3.zeabur.app/swagger/#/Rooms%20-%20%E6%88%BF%E5%9E%8B/get_api_v1_rooms__id_) 來取得房型詳細資料。可以使用 `fetch` 或 `axios` 來串接 API。
- 取得房型資料後，將資料內容渲染在畫面上。畫面的 HTML 、CSS 已有在 `pages/room/_id.vue` 提供。
- 將 pages/notfound.vue 調整成全站的 404 頁面。畫面的 HTML 和 CSS 已經在 `pages/notfound.vue` 中提供。請在 `{{ page }}` 中渲染當前訪問頁面的路由路徑，並提供一個返回首頁的連結。

## 安裝

以下將會引導你如何安裝此專案到你的電腦上。

Node.js 版本建議為：`18.0.0` 以上

### 取得專案

```bash
git clone -b day8-dynamic-router  https://github.com/jasonlu0525/nuxt3-live-question.git day8-dynamic-router-question
```

### 移動到專案內

```bash
cd day8-dynamic-router-question
```

### 安裝套件

```bash
npm install
```

### 運行專案

```bash
npm run dev
```

### 開啟專案

在瀏覽器網址列輸入以下即可看到畫面

```bash
http://localhost:3000/
```

