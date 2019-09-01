<template>
  <div class="hello">
    <p>{{ greet }}</p>
      <p>{{valueLabel}}</p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  name: string = 'Taro'
  value: any = false

  get greet(): string {
    return `Hello ${this.name}`
  }
  get valueLabel(): string {
    return this.value
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
