<!--
Counter Instructions

How many slices of data do you think are necessary to act as "sources of truth" for all
the things that change in this widget? Give it some thought before continuing reading!

STEP 0:
  Start by studying the component below, and setup the data function / method.

STEP 1:
  In the **data** method, create a 'count' property.
  The initial value should be set to 0.

STEP 2:
  The 'style' object in our getStyles method has the 'color' property hard-coded to "royalblue".
  What the value of 'color' should be instead is a vlue changed dynamically, it goes like this:
  If count is even, then "royalblue", else "crimson" and then return the styles object 

STEP 3:
  We need to replace some hard-coded info in the template with expressions, inside mustache syntax (double curly braces).
  Start by replacing the character "0" with {{ count }}. The 'count' slice of data is the source of truth here.
  Then, replace the word "even" with a ternary: {{ if count is even number, then string "even", else string "odd" }}.

  Docs: https://v3.vuejs.org/guide/template-syntax.html#using-javascript-expressions

STEP 4:
  Increment Function

  This click handler needs to set the 'count' to be the current 'count' plus one.

STEP 5:
  Decrement Function

  This click handler needs to set the 'count' to be the current 'count' minus one.

STEP 6:
  Reset Function
  This click handler needs to set the 'count' to be zero again.
-->
<template>
  <div class='widget-counter container'>
      <h2>Counter</h2>
      <div id='count' :style="getStyles()">
        Number 0 is even <!-- Step 3 --> 
      </div>
      <div>
        <button id='increment' @click="increment">Increment</button>
        <button id='decrement' @click="decrement">Decrement</button>
        <button id='resetCount' @click="reset">Reset</button>
      </div>
    </div>
</template>

<script>
export default {
    name: "Counter",
    data() {
        return {
          // Step 1

        }
    },
    methods: {
        getStyles() {

            const styles = {
              fontSize: '1.5em',
              marginBottom: '0.3em',
              color: 'royalblue' // Step 2 
            }

            return styles
        },
        increment() {
            // Step 4
        },
        decrement() {
            // Step 5
        },
        reset() {
            // Step 6
        }
    }
}
</script>