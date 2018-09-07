<template>
  <div>
    <h3>Rendering Lists - v-for</h3>
      <ul>
        <h5>Ingredients</h5>
        <li v-for="(ingredient, i) in ingredients" :key="ingredient">
        <span>{{i + 1}}: </span>{{ ingredient }}</li>
      </ul>

      <button @click="ingredients.push('spices')">Push Item</button>

      <ul>
        <h5>Persons</h5>
        <li v-for="(person, i) in persons"> 
        userId: {{i}} <br>
        Name: {{ person.name }} <br>
        Age: {{person.age}} <br>
        Color: {{person.color}} <br><br>
        </li>
      </ul>

      <ul>
        <h5>Persons V2</h5>
        <li v-for="person in persons"> 
          <div v-for="(value, key, index) in person">
          {{index}}: {{key }}: {{value}}</div>
        </li>
      </ul>

      <hr>

      <h5>Rendering a list of numbers</h5>
      <span v-for="n in 10">{{ n }}</span>
  </div>
</template>

<script>
export default {
  name: "RenderListsVfor",
  data() {
    return {
      ingredients: ["steak", "fruits", "veggies", "milk", "cream"],
      persons: [
        { name: "Max", age: "22", color: "red" },
        { name: "Sean", age: "30", color: "black" },
        { name: "John", age: "31", color: "blue" },
        { name: "Toby", age: "28", color: "yellow" }
      ]
    };
  }
};
</script>

<style scoped>
ul {
  list-style-type: none;
}
</style>
