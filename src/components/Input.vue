<!--
Input Instructions

STEP 0:
  Study the component below and get familiar with what is already setup.

STEP 1:
  Create a data property called 'inputValue' and set it to a empty string

STEP 2:
  Make the color of the text be crimson if the length of 'inputValue' goes over ten.

STEP 3:
  Interpolate the value of the input inside the div with an id of 'output'. How can we make it show in ALL CAPS?

  Docs: https://v3.vuejs.org/guide/template-syntax.html#using-javascript-expressions

STEP 4:
  Using the v-model, bind to the 'input' data property on our input field that has the id of 'input'

STEP 5:
  Set the 'input' data attribute to be empty string. 

-->
<template>
    <div class='widget-input container'>
      <h2>Input</h2>
      <div id='output' v-bind:style="getStyles()"></div> <!-- Step 3 -->
      <div>
        <input id='input' type='text' /> 
        <button id='resetInput' v-on:click="reset">Reset</button>
      </div>
    </div> 
</template>

<script>
export default {
    name: 'Input',
    data() {
        // Step 1
        return {

        }
    },
    methods: {
        getStyles() {
            const styles = {
                fontSize: '1.5em',
                marginBottom: '0.3em',
                color: 'royalblue', /* STEP 2 */ 
            }

            return styles
        },
        reset() {
            // Step 5

        }
    }

}
</script>

<style>

</style>