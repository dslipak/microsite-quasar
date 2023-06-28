<template>
  <div class="fullscreen text-white text-center q-pa-md flex flex-center app-global">
    <div>
      <div style="font-size: 10vh">
        404
      </div>

      <div class="text-h4" style="opacity:.4">
        Oops. Nothing here...
      </div>

      <q-btn
        class="q-mt-xl"
        color="dark"
        text-color="white"
        unelevated
        to="/"
        label="Go Home"
        no-caps
      />
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'ErrorNotFound'
})
</script>
