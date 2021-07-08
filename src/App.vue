<template>
  <div class="app"> 
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('Mely')">change name</button>
    <button @click="changeAge(32)">change age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from 'vue';

export default defineComponent({
  name: 'App',
  components: {},
  setup() {
    // const state = reactive({
    //   name: "Link",
    //   age: 25 as string | number
    // })

    // state.name = "Shaun";
    // state.age = '25';

    // return { ...toRefs(state) }

    const name = ref("Link")
    const age = ref<number | string>(25)


    
    return { name, age }
  },
  methods: {
    changeName(name: string) {
      this.name = name
      return name
    },
    changeAge(age: number | string ) {
      this.age = age
      return age
    }
  }
});
</script>

<style>
</style>
