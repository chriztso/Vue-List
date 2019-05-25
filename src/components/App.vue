<template>
  <div class="whole">
    <div>
      {{message}}
    </div>
    <div>
      <button v-on:click = "reverseMessage">Reverse</button>
    </div>  
    <div>
      <ol> 
        <li v-for="todo in todos"> 
          {{todo.text}}
        </li>
      </ol>  
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "Chris's List", 
      todos : [
          {text : 'Eat dinner'},
          {text : 'Buy books'}, 
          {text : 'Go to class'}
      ]
    }
  },
  methods: {
    reverseMessage: function () {
      this.message = this.message.split('').reverse().join('')
    }
  },
};
</script>


<style>
.whole{
    display: flex;
    flex-direction: column;
    border: 1px solid black;
    padding-left: 600px;
}
</style>