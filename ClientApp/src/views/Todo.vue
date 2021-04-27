<template>
<div>
    <input v-model="addTodo" placeholder="Add todo">
<v-checkbox v-model="checkbox" :label="`Todo 1: ${checkbox.toString()}`"></v-checkbox>
</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {  }
})
export default class App extends Vue {

    checkbox = true
    addTodo = "Jotain"


}
</script>