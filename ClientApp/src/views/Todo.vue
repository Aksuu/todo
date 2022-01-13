<template>
  <div>
    <!-- <v-text-field label="To Do" @keydown.enter="addTodo()" v-model="toDoItem" placeholder="Write here" />
    <v-btn @click="addTodo()" color="primary">Add item</v-btn> -->
    <form class="col-12" @submit.prevent="addTodo()">
    <input
      v-model="toDoItem"
      type="text"
      class="form-control"
      placeholder="Add todo"
    />
  </form>

    <div v-show="hide">
    <li v-for="(item, index) in items" v-bind:key="index">
      <v-row class="mt-2 ml-2" align="center">
      <v-checkbox @click="checkboxClick()" :label="item" />
      <v-btn class="my-4 ml-8" @click="editTodo(index)" color="primary">Edit</v-btn>
      <v-btn class="my-2 ml-2" @click="removeTodo(index)" x-small fab color="red">X</v-btn>
      </v-row>
    </li>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
import CreateItem from '@/components/CreateItem.vue'
import Todo from '@/components/Todo.vue'

@Component({
  components: { CreateItem, Todo}
})
export default class App extends Vue {

  get hide(): boolean {
    if (this.hide) {
      return true
    } else {
      return false
    }
  }

  public addTodo(): void {
    this.addTodo
  }

  public removeTodo(index: number): void {
    this.removeTodo
  }

  //TODO: Kirjoita stepit edit-toiminnolle! Logiikka!
  // Text-fieldin muuttaminen inputtiin (toimiiko nykyinen logiikka samalla tavalla inputin kanssa?)
      // input on formin sisällä ja kaikki listan sisälle
      // checkboxin "sisälle" input-field, johon tulee todo arvo
  // finishedit -nappi, joka tallentaa uuden arvon
  // inputille v-if, joka katsoo kummassa tilassa ollaan (edit vai ei)
  // Tee omat komponentit!
    // Mille kaikille voi tehdä komponentit?
  // Tsekkaa dokumentit

    public editTodo(index: number): void {

    console.log()
  }
}
</script>
