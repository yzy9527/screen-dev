<script>
import { reactive, watchEffect } from 'vue'

const state = reactive({
  count: 1
})

watchEffect(() => {
  document.body.innerHTML = `count:${state.count}`
})
</script>
