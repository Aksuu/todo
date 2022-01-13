<template>
<form class="col-12" @submit.prevent="addTodo()">
  <input
    v-model="toDoItem"
    type="text"
    class="form-control"
    placeholder="Add todo"
  />
</form>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {}
})
export default class App extends Vue {
  items = new Array<string>()
  toDoItem = ''

  // beforerouteenter?

  get hide(): boolean {
    if (this.items.length > 0) {
      return true
    } else {
      return false
    }
  }

  public addTodo(): void {
    // Lisää arrayhin uusi checkbox element, määrittele mitä se ottaa
      this.items.push(this.toDoItem)
      this.toDoItem = ''

      console.log(this.toDoItem)
  }
}
</script>
