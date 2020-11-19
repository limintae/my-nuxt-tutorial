<template>
  <div>
    <h2>Counter: {{ this.$store.state.helloWorld.counter }}</h2>
    <h2>
      Counter: {{ this.$store.state.samples.counter.sampleCounter.counter }}
    </h2>
    <button @click="add_one">Add counter</button>
    <button @click="addSampleCounter">Add sample counter</button>
  </div>
</template>

<script>
export default {
  methods: {
    add_one() {
      this.$store.commit('helloWorld/increment')
    },
    addSampleCounter() {
      this.$store.commit('samples/counter/sampleCounter/increment')
    },
  },
}
</script>
