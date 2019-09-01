<template>
  <div class="hello">
    <p>{{ greet }}</p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
@Prop({ type: Boolean, default: false})
flag!: boolean

@Prop({ type: [String,Number],default :null})
message!: string | null

@Prop({ type: [String, Number], default: null })
value!: string | number | null
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
