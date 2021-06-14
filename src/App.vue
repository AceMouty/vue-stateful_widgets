<template>
  <Counter/>
  <Input />
</template>

<script>
import Counter from './components/Counter.vue';
import Input from './components/Input.vue';
export default {
  name: 'App',
  components: {
    Counter,
    Input
  }
}
</script>
