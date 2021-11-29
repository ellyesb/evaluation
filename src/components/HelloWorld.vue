<template>
  <div class="hello">
 
 <p v-if="errors.length">
      <b>Please correct the following error(s):</b>
      <ul>
        <li v-for="error in errors" :key="error">{{ error }}</li>
      </ul>
    </p>
 <label for="start">Start date:</label>

<input type="date" id="start" name="trip-start"
       value="2018-07-22"
       min="2018-01-01" max="2018-12-31">

       <p>Select a maintenance drone:</p>

<div>
  <input type="radio" id="9:30" name="drone" value="9:30"
         checked>
  <label for="9:30">9:30</label>
</div>

<div>
  <input type="radio" id="10:30" name="drone" value="10:30">
  <label for="10:30">10:30</label>
</div>

<div>
  <input type="radio" id="11:30" name="drone" value="11:30">
  <label for="11:30">11:30</label>
</div>

<div>
  <input type="radio" id="12:30" name="drone" value="12:30">
  <label for="12:30">12:30</label>
</div>
 
 <div>
  <input type="radio" id="13:30" name="drone" value="13:30">
  <label for="13:30">13:30</label>
</div>

<div>
  <input type="radio" id="14:30" name="drone" value="14:30">
  <label for="14:30">14:30</label>
</div>
  
  <div>
  <input type="radio" id="15:30" name="drone" value="15:30">
  <label for="15:30">15:30</label>
</div>
  
  <div>
  <input type="radio" id="16:30" name="drone" value="16:30">
  <label for="16:30">16:30</label>
</div>
  
  <div>
  <input type="radio" id="17:30" name="drone" value="17:30">
  <label for="17:30">17:30</label>
</div>
    <form id="App" 
    @submit="checkForm"
    method="post">

    
    <p>
      <input type="submit" value="Submit">
    </p>
  </form>
    
    </div>


</template>

<script>

export default {
  name: 'App',
  components: {

  },
  data() {
    return {
      errors: [],
      start: null,
      date: null,
      
    }
  },
  methods: {
    checkForm: function(e) {

      // Clear errors
      this.errors = [];

      // Check if the surname is not empty and length <= 50
      if (!this.xq || this.start.length > 0)
      {
        this.errors.push("choisir une heure");
      }

      // Check if the firstname is not empty and length <= 50
      if (!this.radio || this.radio.length > 0)
      {
        this.errors.push("choisir une date");
      }

     

      if (!this.errors.length)
      {
        return true;
      }

      e.preventDefault();
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
