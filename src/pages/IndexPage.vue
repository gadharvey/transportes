<script setup lang="ts">
import { ref } from 'vue'
import type { Todo, Meta } from 'components/models'
import ExampleComponent from 'components/ExampleComponent.vue'

const todos = ref<Todo[]>([
  {
    id: 1,
    content: 'ct1',
  },
])

const meta = ref<Meta>({
  totalCount: 1200,
})
</script>
<template>
  <q-page class="row items-center justify-evenly">
    <example-component
      title="Example component"
      active
      :todos="todos"
      :meta="meta"
    ></example-component>
  </q-page>
</template>
