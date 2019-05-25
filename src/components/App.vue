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
    <div>
      <input v-model="messageOne" placeholder="type something">
      <p> Message is: {{messageOne}}</p>
    </div>
    <div>
      <input type="checkbox" id="Homework1" value="Homework1" v-model="homework">
      <label for="Homework1">Homework1</label>
      <input type="checkbox" id="Homework2" value="Homework2" v-model="homework">
      <label for="Homework2">Homework2</label>
      <input type="checkbox" id="Homework3" value="Homework3" v-model="homework">
      <label for="Homework3">Homework3</label>
      <br>
      <span> Homework complete: {{homework}} </span>
    </div> 
  </div>
</template>

<script>
export default {
  data() {
    return {
      homework: [],
      messageOne: '',
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