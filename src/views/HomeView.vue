<template>
  <main>
  <div class="texts" v-for="item in items" :key="item">
    <p :class="{active:isActive}">меня зовут {{ item.name }} моя фамилия {{item.surname}}</p>
    <p>мне {{item.age}} я учусь {{item.company}}</p>
    <button  v-on:click="isActive =!isActive">Click me!</button>
  </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      items:[{name: "ксюша", surname: "христюк", age: "16", company: "шаг"}],
      isActive: false
    }
  }
}
</script>

<style>
 .texts{
  font-weight: 600;
  font-size: large;
}
.active{
  background-color: pink;
  color: white;
}

</style>
