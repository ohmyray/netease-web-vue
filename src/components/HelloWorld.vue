<template>
  <a-button type="primary">Primary</a-button>
  <a-button>Default</a-button>
  <a-button type="dashed">Dashed</a-button>
  <a-button type="danger">Danger</a-button>
  <a-button type="primary">按钮</a-button>
  <a-button type="link">Link</a-button>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
export default defineComponent({
  name: 'HelloWorld',
  props: {
    msg: {
      type: String,
      required: true
    }
  },
  setup: () => {
    const count = ref(0)
    return { count }
  }
})
</script>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
