<!--
Spinner Instructions

How many data properties do you think are necessary to act as "sources of truth" for all
the things that change in this widget? Give it some thought before continuing reading!

Our first impulse might be to say 2 different properties:
  - Whether the spinner is visible or not (perhaps this could be a boolean).
  - Whether the text of the button reads "Show Spinner" or "Hide Spinner".

But a single data property is all that's needed here: whether spinner is on or not.
The text of the button can be derived from the value of that one data property.

STEP 0:
  Start by studying the component below, and setting up the data method.

STEP 1:
  Create a 'spinnerOn' data property.
  The 'spinnerOn' should be initialized to true so the spinner is visible on page load.

STEP 2:
  This is called conditional rendering. If the expression is truthy,
  the piece of tempate will show up on the page. If the expression is falsy, 
  the template piece will not show up. It's a neat little trick to render
  a element (in this case the spinner) conditionally: only if the is truthy.

  Replace the hard-coded 'true' with the variable that keeps track of whether spinner is on or not.

STEP 3:
  Use a ternary expression inside the text of the button, to render "Hide" or "Show" depending on the value of 'spinnerOn'.

STEP 4:
  This click handler needs to toggle the spinner by setting "the on / off state" to be the opposite of what it currently is.
  Do you remember the logical operator we use to do "not"?
-->

<!-- Step 0 -->
<template>
    <div class='widget-spinner container'>
      <h2>Spinner</h2>
        <div v-if="true" id='spinner' class='spinner'>--+--</div> <!-- STEP 2 -->
      <button id='toggleSpinner' v-on:click="toggleSpinner">
        Hide Spinner <!-- STEP 3 -->
      </button>
    </div> 
</template>

<script>
export default {
    name: "Spinner",
    data() {
        return {
            // Step 1
            
        }
    },
    methods: {
        toggleSpinner() {
            // Step 4
        }
    }
}
</script>