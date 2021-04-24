<template lang="html">
  <div class="w3-hover-shadow w3-panel w3-leftbar w3-light-grey" style="height: 623px;"><br>
  <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
  <button class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" v-on:click="bintodec(); bintooct(); bintohex();" style="width: 49%">Binary to Decimal</button>
  <button class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" v-on:click="reset()" style="width: 49%">clear all the fields</button><br><br>
    <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll"><b>Conversion:</b> {{ ans }}</p>
    <h3><b>{{ text_value }} to base-8</b></h3>
    <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll"><b>Conversion:</b> {{ ansoct }}</p>
    <h3><b>{{ text_value }} to base-16</b></h3>
    <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll"><b>Conversion:</b> {{ anshex }}</p>
  </div>
</template>

<script>
import { BigNumber } from 'bignumber.js';
export default {
data () {
  return {
    text_value: null,
          ans: "",
          anshex: "",
          ansoct: ""
  }
},
methods: {
  bintodec() {
    var cc = new BigNumber(this.text_value, 2);
     this.ans = cc;
   },
   bintohex() {
     var bin = this.text_value;
     var m = new BigNumber(bin, 2)
     var binn = m.toString(16);
     this.anshex = binn;
           },
           bintooct() {
             this.aaa = parseInt(this.text_value);
             var bintooct = parseInt(this.aaa, 2).toString(8);
             this.ansoct = bintooct;
                   },
 reset() {
   this.ans = '',
   this.text_value= null,
   this.ansoct = '',
   this.anshex = ''
 }
}
}
</script>

<style lang="css">
</style>
