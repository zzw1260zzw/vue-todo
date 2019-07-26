<template>
  <div>
      <div :key="index" v-for = "(todo,index) in  todos">
        <Todoitem :todo="todo" @deleteItem="$emit('handleDelete',todo.id)"/>
      </div>
  </div>
</template>

<script>
import Todoitem from "./Todoitem"
export default {
  name:"Todos",
  props:["todos"],
  components:{
    Todoitem
  },
  // methods:{
  //   deleteItem(id){
  //     console.log(id);
  //   }
  // }
};
</script>

<style scoped>
  
</style>