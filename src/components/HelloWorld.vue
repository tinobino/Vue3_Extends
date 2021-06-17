<template>
  <SubComponent />
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import SubComponent from '@/components/SubComponent.vue'

export default defineComponent({
  name: 'HelloWorld',
  components: {
    SubComponent
  }
})
</script>
