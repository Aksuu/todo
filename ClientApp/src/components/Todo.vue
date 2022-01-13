<template>
<div v-show="hide">
  <li v-for="(item, index) in items" v-bind:key="index">
    <v-row class="mt-2 ml-2" align="center">
      <v-checkbox @click="checkboxClick()" :label="item" />
      <v-btn class="my-4 ml-8" @click="editTodo(index)" color="primary">Edit</v-btn>
      <v-btn class="my-2 ml-2" @click="removeTodo(index)" x-small fab color="red">X</v-btn>
    </v-row>
  </li>
</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {}
})
export default class App extends Vue {
  items = new Array<string>()
  checkbox = false

  public checkboxClick(): void {
    this.checkbox = true
  }

  public removeTodo(index: number): void {
    this.items.splice(index, 1)
    console.log(this.items)
  }

  public editTodo(index: number): void {
    console.log(this.items)
  }
}
</script>
