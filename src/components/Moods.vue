<!--
Moods Instructions

STEP 0:
  Study the component below, once familiar contiue to next steps 

STEP 1:
  Create a 'mood' data attribute.
  The 'mood' data attribute should be initialized to one of the three variables in our script tag.
  Those variables exist so we don't need to write those long strings anywhere inside the component.

STEP 2:
  Make the color of the text be royalblue if the state of the mood is happy, crimson otherwise.

STEP 3:
  Remove the hard-coded mood and interpolate the 'mood' data atrribute instead, using the mustache syntax (double curly braces).

STEPS 4, 5, 6:
  Inside these click handlers set the correct mood, using the mood variables in our script tag.
-->

<!-- Step 0 -->
<template>
    <div className='widget-moods container'>
      <h2>Moods</h2>
      <div id='mood' v-bind:style="styles">Not sure how I feel</div> <!-- STEP 3 -->
      <div>
        <button id='makeHappy' v-on:click="makeHappy">Make Happy</button>
        <button id='makeSad' v-on:click="makeSad">Make Sad</button>
        <button id='resetMood' v-on:click="reset">Reset</button>
      </div>
    </div> 
</template>

<script>

const initialMood = 'Not sure how I feel';
const happyMood = 'Quite happy!';
const sadMood = 'Rather sad';

export default {
    name: 'Moods',
    data() {
        return {
            styles: {
               fontSize: '1.5em',
                marginBottom: '0.3em',
                color: 'crimson' 
            }
        }
    },
    methods: {
        makeHappy() {

        },
        makeSad() {

        },
        reset() {

        }
    }
}
</script>