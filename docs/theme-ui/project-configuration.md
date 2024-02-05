# 專案配置

## Color

?> 要更改主要顏色和相關色系設定如下：

### 覆蓋主題顏色

如需更改，請前往： src/plugins/vuetify.js <br/>
預設主題色為 default 設定

### 更改主題顏色

如需更改切換的主題色彩及暗黑設定，請前往： src/plugins/vuetify.js <br/>
至對應的主題色更改設定，欲新增主題色彩 也可自定義主題名稱

```javascript
 theme: {
    defaultTheme: "default",
    themes: {
      default: {
        dark: false,
        colors: {
          primary: "#0156a2",
          secondary: "#32a7fa",
          loginColor: "#0156a2",
          light: "#8eebb1",
          navText: "#262626",
          thead: "#dadfe0",
        },
      },
      color1: {
        dark: false,
        colors: {
          primary: "#1e484a",
          secondary: "#1f6053",
          loginColor: "#1e484a",
          light: "#36e79e",
          navText: "#1e484a",
          thead: "#dae0db",
        },
      },
      color3: {
        dark: false,
        colors: {
          primary: "#103d5c",
          secondary: "#0786b2",
          loginColor: "#103d5c",
          light: "#00f0ff",
          navText: "#103d5c",
          thead: "#dadfe0",
        },
      },
      color2: {
        dark: false,
        colors: {
          primary: "#4e0c30",
          secondary: "#852648",
          loginColor: "#4e0c30",
          light: "#ff378c",
          navText: "#4e0c30",
          thead: "#e0dadd",
        },
      },
      dark: {
        dark: true,
        colors: {
          primary: "#fefefe",
          loginColor: "#000",
          secondary: "#695f5f",
          light: "#ff378c",
          thead: "#525252",
        },
      },
    },
  }


```

## Typography

?> 更改主要文字樣式及設定如下:

### Google fonts

如需新增，請前往： / index.html <br/>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@400;500;600&display=swap" rel="stylesheet" />
  </head>

  <body>
    ...
  </body>
</html>
```

### 修改字型樣式

如需修改文字樣式則須至 src / sass / variables.scss

```sass
$fontFamily: 'Noto Sans', 'Noto Sans TC', Lato, 'PingFang TC', 'Helvetica Neue', Helvetica, 微軟正黑體, Arial, sans-serif;
```

## Icons

?> 要更改 Icons 主題及樣式 如下：

### 自行設定 icon

可依照檔案需求，載入所需的 Icon 類型<br>
src / plugins / vuetify.js

> 類型樣式 可參考 [Vuetify 文件](https://vuetifyjs.com/en/features/icon-fonts/#material-icons-css)

```javascript
icons: {
    defaultSet: "mdi",
    aliases,
    sets: {
      fa,
      mdi,
    },
  },
```

### 可外部自行載入 icon

檔案放置位子如下： <br/>
sass / vendor / material-icons-round.scss <br/>
sass / setting.scss <br/>

> 撰寫及載入方式可參閱[ Google Fonts](https://fonts.google.com/icons)

```sass
//material-icons-round
@import '@/sass/vendor/material-icons-round.scss';
```

```html
<span class="material-icons-round"> logout </span>
```

## 響應式斷點

### 使用

此模板 根據 [Vuetify](https://vuetifyjs.com/zh-Hans/components/grids/#section-4f7f7528) 的配置設定。使用 flexbox 建構的 12 格網格系統。網格用於在應用程式的定的佈局。
<br/>包含 5 種斷點來針對特定的螢幕尺寸或方向：xs、sm、md、lg 和 xl。可以透夠需求來調整斷點尺寸。<br/>

> 各元件也可透過 sass 的設定 來調整各斷點的樣式，相關變數連結為：
> sass/common/ mixins/ \_mediaquery.scss

| 裝置     | 名稱 | 類型                   | 範圍              |
| -------- | ---- | ---------------------- | ----------------- |
| 超小尺寸 | xs   | Small to large phone   | < 600px           |
| 小尺寸   | sm   | Small to medium tablet | 600px > < 960px   |
| 中尺寸   | md   | Large tablet to laptop | 960px > < 1280px  |
| 大尺寸   | lg   | Laptop to desktop      | 1280px > < 1920px |
| 超大尺寸 | xl   | 1080p to 1440p desktop | 1920px > < 2560px |
| 超大尺寸 | xxl  | 4k and ultra-wide      | > 2560px          |
