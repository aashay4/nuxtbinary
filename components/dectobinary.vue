<template>
  <div class="w3-hover-shadow w3-panel w3-leftbar w3-light-grey" style="height: 623px;"><br><br>
  <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
  <button class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" v-on:click="dectobin(); dectohex(); dectooct();" style="width: 49%">Convert</button>
  <button class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" v-on:click="reset()" style="width: 49%">clear all the fields</button><br><br>
    <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">Conversion: {{ ans }}</p>
    <h3><b>{{ text_value }} to base-8</b></h3>
    <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">Conversion: {{ ansoct }}</p>
    <h3><b>{{ text_value }} to base-16</b></h3>
    <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">Conversion: {{ anshex }}</p>
  </div>
</template>

<script>
import { BigNumber } from 'bignumber.js';
export default {
  data () {
    return {
      text_value: null,
            ans: "",
            anshex: '',
            ansoct: ''
    }
  },
  methods: {
    dectobin() {
      var x = new BigNumber(this.text_value, 10)
    var dectobin = x.toString(2);
    this.ans = dectobin;
            },
      dectohex() {
            var xzc = new BigNumber(this.text_value, 10)
            var dectohexo = xzc.toString(16).toUpperCase ();
            this.anshex = dectohexo;
                    },
                    dectooct() {
                    var xmm = new BigNumber(this.text_value, 10)
                    var dectoocto = xmm.toString(8);
                    this.ansoct = dectoocto;
                            },
   reset() {
     this.ans = '',
     this.text_value= null,
     this.anshex= '',
     this.ansoct= ''
   },
  }
}
</script>

<style lang="css">
</style>
