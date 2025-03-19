# test-vue-slot-component-package

```
yarn install

yarn build:ui

yarn dev
```

when you at the root of the app project

apps/desktop/src/App.vue

```
<script setup lang="ts">
import { Button1, Button2 } from '@test/ui';
</script>

<template>
  <div>
    <!-- <Button1></Button1> -->
    <Button2></Button2>
  </div>
</template>
```

Button2 is not working, but Button1 is working.

the error message is

```
index.mjs:618 Uncaught TypeError: Cannot read properties of null (reading 'ce')
    at renderSlot (index.mjs:618:32)
    at Proxy._sfc_render (index.mjs:1262:5)
    at renderComponentRoot (chunk-3SZSTCRY.js?v=05012731:8581:17)
    at ReactiveEffect.componentUpdateFn [as fn] (chunk-3SZSTCRY.js?v=05012731:7403:46)
    at ReactiveEffect.run (chunk-3SZSTCRY.js?v=05012731:481:19)
    at setupRenderEffect (chunk-3SZSTCRY.js?v=05012731:7538:5)
    at mountComponent (chunk-3SZSTCRY.js?v=05012731:7313:7)
    at processComponent (chunk-3SZSTCRY.js?v=05012731:7266:9)
    at patch (chunk-3SZSTCRY.js?v=05012731:6782:11)
    at mountChildren (chunk-3SZSTCRY.js?v=05012731:7014:7)
```