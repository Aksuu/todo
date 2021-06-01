<template>
<div>
    <v-text-field label="To Do"  placeholder="Write here"/>
    <v-btn @click="addTodo" color="primary">Add item</v-btn>
    <li v-for="item in items" v-bind:key="item">
    <v-checkbox v-model="checkbox" :label="`Todo 1: ${checkbox.toString()}`"></v-checkbox>
    </li>
</div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component({
  components: {  }
})
export default class App extends Vue {

  items = new Array<string | undefined>()
 
  public addTodo() : void {

    // Lisää arrayhin uusi checkbox element, määrittele mitä se ottaa

    console.log(this.addTodo)
 }
 checkbox = "";

}
</script>