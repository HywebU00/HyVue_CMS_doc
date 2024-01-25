# Routing

#### 新增路線

如需更改，請前往： src / router / index.js <br/>

```javascript
// ----------------------------------------------------
// File: src / router / index.js
// ----------------------------------------------------

const routes = [
  {
    path: '/',
    component: () => import('@/views/layout/adminLayout.vue'),
    children: [
      {
        path: 'system',
        component: () => import('@/views/admin/systemComponent.vue'),
      },
      {
        path: 'component',
        component: () => import('@/views/admin/Component.vue'),
      },
      ...
    ],
  },
];
```

#### 新增側邊欄位

如需更改，請前往： src / views / layout / adminLayout.vue <br/>

```html
<v-navigation-drawer>
  <v-list>
    <v-list-group value="Home1">
      <template v-slot:activator="{ props }">
        <v-list-item title="Home" @click="pushLink('/')"> </v-list-item>
      </template>
    </v-list-group>
  </v-list>
  ...
</v-navigation-drawer>
```
