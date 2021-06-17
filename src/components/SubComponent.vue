<template>
  <ul>
    <li>abstractProp: {{ abstractProp }}</li>
    <li>foo: {{ foo }}</li>
    <li>myProp: {{ myProp }}</li>
  </ul>
</template>

<script lang="ts">
import { computed, defineComponent, toRefs } from 'vue'
import AbstractComponent from './AbstractComponent.vue'

export default defineComponent({
  name: 'SubComponent',
  extends: AbstractComponent,
  props: {
    foo: {
      type: String,
      default: 'bar'
    }
  },
  setup(props){
    const { abstractProp, foo } = toRefs(props);

    const myProp = computed( () => `${foo.value}_${abstractProp.value}`)

    return {
      myProp
    }
  }
})
</script>
