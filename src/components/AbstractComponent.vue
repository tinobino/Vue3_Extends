<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'AbstractComponent',
  props: {
    abstractProp: {
      type: String,
      default: 'abstractProp'
    }
  }
})
</script>
