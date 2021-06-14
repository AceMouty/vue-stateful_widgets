<!--
Programmers Instructions

This component keeps track of a list of pioneers in the field of programming,
and the id of the currently featured programmer. That's two data properties!
We can only feature one awesome programmer at a time.

Find comments below to help you along.
-->
<template>
    <div class='widget-programmers container'>
      <h2>Programmers</h2>
      <div class='programmers'>
       <!-- 
          Nasty bug! We should loop over a data property, instead of 'listOfAwesome'.
          We might think: "it works, though!" But if the list of programmers is not a data property,
          we could never add or edit programmers in the future. It would look as if nothing happened 
       --> 
       <div class="programmer" v-for="dev in listOfAwesome" v-bind:key="dev.id">
           {{ dev.name }}
           <button v-on:click="() => { /* in here set the featured id to be the dev.id*/}">Feature</button>
       </div>
      </div>
      <div id='featured' v-bind:style="getStyles()">
        {{
          // Ternaries are fantastic to render "one thing or the other" depending on the "truthiness" of something.
          // Pseudo-code: if the currently featured id is truthy render text 1, otherwise render text 2.
          // Replace the hard-coded false with the correct variable.
          false
            ? `🎉 Let's celebrate ${getNameOfFeatured()}! 🥳`
            : 'Pick an awesome programmer'
        }}
      </div>
    </div> 
</template>

<script>
const listOfAwesome = [
  { id: '1', name: 'Ada Lovelace' },
  { id: '2', name: 'Grace Hopper' },
  { id: '3', name: 'Evelyn Boyd Granville' },
  { id: '4', name: 'Mary Kenneth Keller' },
  { id: '5', name: 'Frances Allen' },
  { id: '6', name: 'Carol Shaw' },
];
export default {
    name: 'Programmers',
    data() {
        return {
            
        }
    },
    methods: {
        getStyles() {
            const styles = {
              fontSize: '1.5em',
              marginTop: '0.5em',
              color: 'royalblue' // 🤔 color should turn to gold, when celebrating 
            }

            return styles
        },
        getNameOfFeatured() {
            // Leave this for last!
            // This is NOT an event handler but a helper function. See its usage inside the template.
            // It's going to utilize both data properties to return the _name_ of the featured dev.
        }
    }
}
</script>