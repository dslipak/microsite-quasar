<template>
  <router-view />
</template>

<script>
import { defineComponent } from 'vue'
import { useQuasar } from 'quasar'
import api from './services/api'

export default defineComponent({
  name: 'App',

  setup () {
    const $q = useQuasar()

    return {
      showNotif (message) {
        $q.notify({
          message: message,
          color: 'dark',
          position: 'top'
        })
      }
    }
  },

  beforeMount () {
    const self = this
    api.ping()
      .then(response => {
        console.log(response)
        if (response.status != 200) {
          self.showNotif('can\'t connect to backend')
        }
      })
      .catch(error => {
        console.log(error)
      })
  }
})
</script>
