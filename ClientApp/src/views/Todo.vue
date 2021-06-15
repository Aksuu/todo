<template>
  <div>
    <v-text-field label="To Do" v-model="toDoItem" placeholder="Write here" />
    <v-btn @click="addTodo()" color="primary">Add item</v-btn>
    <li v-for="(item, index) in items" v-bind:key="index">
      <v-checkbox v-model="checkbox" :label="item"></v-checkbox>
    </li>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {}
})
export default class App extends Vue {
  items = ['']
  checkbox = ''
  toDoItem = ''

  public addTodo(): void {
    // Lisää arrayhin uusi checkbox element, määrittele mitä se ottaa
      
      this.items.push(this.toDoItem)

      console.log(this.checkbox)
      console.log(this.toDoItem)
      console.log(this.items)
  }
}
</script>
