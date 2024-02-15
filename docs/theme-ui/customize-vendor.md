# 套件配置

## 動態效果 / GSAP 運用

?> 模板動態效果可參考 GSAP 或是其他相關套件 <br/>

模板運用效果 如: `animateNumber`效果 <br/>
相關設定 請詳閱 [GSAP](https://gsap.com/) 套件

在檔案中引入套件

```javascript
src / views / admin / defaultComponent.vue;
import gsap from 'gsap';
```

引入套件

```bash
npm install gsap
```

<hr style="margin-bottom:8rem;"/>

## 圖表 / apexcharts 運用

?> 模板中圖表設定可參考 charts 或是其他相關圖表套件

相關圖表設定 請詳閱 [apexcharts](https://apexcharts.com/vue-chart-demos/) 套件

<img  src="doc_img/img_chart.png"></img>

安裝套件

可參考相關[文件連結](https://apexcharts.com/docs/vue-charts/)

```bash
npm install --save apexcharts
npm install --save vue3-apexcharts
```

在專案中 引入套件

```javascript
//main.js
import VueApexCharts from 'vue3-apexcharts';
```

引入元件

```vue
<template>
  <apexchart type="line" :options="options" :series="series"></apexchart>
</template>
```

<hr style="margin-bottom:8rem;"/>

## 編輯器 / VueQuill 運用

<img style="max-width:860px;" src="doc_img/img_editor.png"></img>

?> 模板中樣式可參考 VueQuill 或是其他相關圖表套件

相關套件設定 請詳閱 [VueQuill](https://vueup.github.io/vue-quill/) 套件

在檔案中引入套件

```javascript
src / views / admin / fromComponent.vue;
import { QuillEditor } from '@vueup/vue-quill';
import '@vueup/vue-quill/dist/vue-quill.snow.css';
```

引入套件

```bash
npm install @vueup/vue-quill@latest
```

引入元件

```vue
<template>
  <quill-editor></quill-editor>
</template>
```

<hr style="margin-bottom:8rem;"/>

## 日期選擇器 / Vue Datepicker 運用

<img style="max-width:600px;" src="doc_img/img_datepicker.png"></img>

?> 模板中樣式可參考 Vue Datepicker 或是其他相關圖表套件

相關套件設定 請詳閱 [Vue Datepicker](https://vue3datepicker.com/props/modes/) 套件

在檔案中引入套件

```javascript
src / views / admin / fromComponent.vue;
import VueDatePicker from '@vuepic/vue-datepicker';
import '@vuepic/vue-datepicker/dist/main.css';
```

引入套件

```bash
npm install @vuepic/vue-datepicker
```

引入元件

```vue
<template>
  <VueDatePicker class="multiDatePicker"></VueDatePicker>
</template>
```
