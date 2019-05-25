<template>
  <div class="whole">
    <div>
      Chris's List
    </div>
    <ol> 
      <li v-for="todo in todos"> 
        {{todo.text}}
      </li>
    </ol>  
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'Hello World', 
      todos : [
          {text : 'Eat dinner'},
          {text : 'Buy books'}, 
          {text : 'Go to class'}
      ]
    }
  }, 
};
</script>


<style>
.whole{
    display: flex;
    flex-direction: column,;
    border: 1px solid black;
    padding-left: 600px;
}
</style>