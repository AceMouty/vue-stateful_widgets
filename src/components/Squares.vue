<!--
Squares Instructions

This component keeps track of a list of "square ids",
and the currently active id. That's two data properties!
One is used as the source of truth to render the squares, and the other
so that the component knows which square is currently active.

Only one square (or none) can be active at any given point.

Find comments below to help you along
-->
<template>
    <div class='widget-squares container'>
      <h2>Squares</h2>
      <div class='squares'>
        <!--
          Nasty bug! We should map over a slice of state, instead of 'listOfSquareIds'.
          We might say: "it works, though!" But if the list of squares is not state,
          we could never add squares, change squares or remove squares in the future. Fix!
        -->
        <div
            v-for="id in lisOfSquareIds"
            v-bind:key="id"
            v-bind:id="id"
            v-bind:class="getComputedClass(id)"
            v-on:click="() => markActive(id)"
            class="squares"
        ></div>
      </div>
    </div> 
</template>

<script>

// Use this only to initialize the deafult value of a data property
const listOfSquareIds = ['sqA', 'sqB', 'sqC', 'sqD'];

export default {
    name: "Squares",
    data() {
        return {

       }
    },
    methods: {
        getComputedClass(id) {
          /*
            This is NOT a click handler but a helper, used inside the template (see above).
            It should return a object containing a key/property named 'active'.
            If the id passed as the argument matches the active square in our data property,
            set 'active' to true, set it to false otherwise.
            Right-click and "inspect element" on the square to see its effect.
          */
        },
        markActive(id) {
            // This is a helper used inside an _inline_ click handler (see above).
            // Set the id argument to become the active id in our data property
            // (unless it already is, in which case we should reset
            // the currently active square id back to initial state).
        }
    }
}
</script>