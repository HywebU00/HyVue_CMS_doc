# 客製化主題

## SCSS 配置

?> 當需要修改模板樣式時

檔案位置如:src/sass<br/>

```text
├── sass/
   ├── common/mixins                  // 相關mixin
   │   ├── _mediaquery.scss
   │   └── _text.scss
   ├── components/                    // Vuetify元件修改
   │   ├── _VListItem.scss
   │   └── _VTable.scss
   ├── customizingComponents/         // 客製化元件修改
   │   ├── card.scss
   │   ├── form.scss
   │   ├── treeBlock.scss
   │   └── table.scss
   ├── layout/                        // 基本模板頁面
   │   ├── customize_color.scss       // 客製化色彩設定
   │   ├── customize_font.scss        // 客製化字型大小設定
   │   └── layout.scss                // 基本模板ＣＳＳ設定
   ├── vendor/                        // 相關支援檔案
   │   └── material-icons-round.scss  // google icon css
   ├── variables.scss                 // 變數
   └── settings.scss                  // 統一匯出之主要SCSS


```

## 模板功能設定

### 切換主題色彩

?> 當需要修改切換主題顏色配置功能時

檔案位置如:src/components/functionNavigation.vue <br/>
若需要更詳細文件 可參考 [ Vuetify Theme ](https://vuetifyjs.com/en/features/theme/#changing-theme)

```vue
<template>
  <v-btn @click="changeTheme('default')">button</v-btn>
</template>
<script>
export default {
  methods: {
    changeTheme(color) {
      let th = this.$vuetify.theme.global;
      th.name = color;
      this.theme = color;
      this.themeDark = false;
      this.createCookie('Theme', `${color}`, 356);
    },
    createCookie(name, value, days) {
      let _expires;
      const _date = new Date();
      if (days) {
        _date.setTime(_date.getTime() + days * 24 * 60 * 60 * 1000);
        _expires = '; expires=' + _date.toGMTString();
      } else {
        _expires = '';
      }
      document.cookie = name + '=' + value + _expires + '; path=/';
    },
  },
};
</script>
```

### 切換字體大小

?> 當需要修改切換主題顏色配置功能時

檔案位置如:src/components/functionNavigation.vue <br/>

```vue
<template>
  <v-btn @click="fontSizeChange('medium')"> 中 </v-btn>
</template>
<script>
export default {
  methods: {
    changeFontSizeClass(targetName) {
      const body = document.querySelector('body');
      switch (targetName) {
        case 'small':
          body.classList.remove('largeSize', 'mediumSize');
          body.classList.add('smallSize');
          this.fontSize = 'small';
          break;
        case 'medium':
          body.classList.remove('smallSize', 'largeSize');
          body.classList.add('mediumSize');
          this.fontSize = 'medium';
          break;
        case 'large':
          body.classList.remove('smallSize', 'mediumSize');
          body.classList.add('largeSize');
          this.fontSize = 'large';
          break;
      }
      this.getFontSizeText(targetName);
    },
  },
};
</script>
```

## 套件配置

### 動態效果 / GSAP 運用

?> 模板動態效果可參考 GSAP 或是其他相關套件 <br/>

模板運用效果 如: `animateNumber`效果 <br/>
相關設定 請參考 [GSAP](https://gsap.com/) 套件

### 圖表 / ECharts 運用

?> 模板中圖表設定可參考 charts 或是其他相關圖表套件

相關圖表設定 請參考 [echarts.js](https://echarts.apache.org/zh/index.html) 套件
