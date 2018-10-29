<template>
  <div class="component">
    <h1>This is an component page</h1>
    <list :items="shapes" title="Shapes">
      <template scope="shape">
        <div>{{shape.name}}</div>
        <small>{{shape.sides}}sides</small>
      </template>
    </list>
    <br>
    <list :items="colors" title="Colors">
      <template scope="color">
        <div>{{color.name}}</div>
        <small>hex:{{color.hex}}</small>
      </template>
    </list>
  </div>
</template>

<script>
// @ is an alias to /src
import List from "@/components/List.vue";

export default {
  name: "home",
  components: {
    List
  },
  data() {
    return {
      shapes: [
        { name: 'Square', sides: 4 }, 
        { name: 'Hexagon', sides: 6 }, 
        { name: 'Triangle', sides: 3 }
      ],
      colors: [
        { name: 'Yellow', hex: '#F4D03F', },
        { name: 'Green', hex: '#229954' },
        { name: 'Purple', hex: '#9B59B6' }
      ]
    }
  }
};
</script>
