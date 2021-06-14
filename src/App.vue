<template>
  <Counter/>
  <Input />
  <Moods />
  <Programmers />
  <Spinner /> 
  <Squares />
</template>

<script>
import Counter from './components/Counter.vue';
import Input from './components/Input.vue';
import Moods from './components/Moods.vue';
import Programmers from './components/Programmers.vue';
import Spinner from './components/Spinner.vue';
import Squares from './components/Squares.vue';

export default {
  name: 'App',
  components: {
    Counter,
    Input,
    Moods,
    Programmers,
    Spinner,
    Squares    
  }
}
</script>
