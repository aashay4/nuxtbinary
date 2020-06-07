<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Decimal to Hexadecimal</h1>
          <p>Converting decimal to hexadecimal number is not a difficult task anymore. You can use our free tool for conversion. Enter a decimal value into the text box if you want to convert decimal to hex and click on the button to get the correct conversion. For example, enter "8888" and click on the conversion button and you will get "22B8" answer.</p>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button v-on:click="dectohex()" style="width: 49%">Decimal to Hexadecimal</button>
          <button v-on:click="reset()" style="width: 49%">clear all the fields</button><br><br>
          <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">Conversion: {{ ans }}</p>
        </div><br>
        <div class="w3-third w3-container">
          <h3 style="background-color: silver;">Other Useful Tools</h3>
          <ul>
            <router-link to="/">
              <li>
                Binary to Text
              </li>
            </router-link>
            <router-link to="/ascii-to-binary/">
            <li>ASCII to Binary</li>
          </router-link>
          <router-link to="/binary-to-decimal/">
          <li>Binary to Decimal</li>
        </router-link>
            <router-link to="/binary-to-hexadecimal/">
            <li>Binary to Hexadecimal</li></router-link>
            <router-link to="/decimal-to-hexadecimal/">
            <li>Hexadecimal to Decimal</li></router-link>
            <router-link to="/decimal-to-octal/">
            <li>Decimal to Octal</li></router-link>
            <router-link to="/binary-to-octal/">
            <li>Binary to Octal</li></router-link>
            <router-link to="/hexadecimal-to-octal/">
            <li>Hexadecimal to Octal</li></router-link>
            <router-link to="/qr-code-generator/">
            <li>QR Code Generator</li></router-link>
            <router-link to="/qr-code-reader/">
            <li>QR Code Reader</li></router-link>
          </ul><br><br>
          <h3 style="background-color: silver;">Useful Resources</h3>
          <ul>
            <router-link to="/about-creator/">
            <li>About</li>
          </router-link>
            <router-link to="/blog/">
            <li>Blog</li>
          </router-link>
          </ul>
        </div>
      </div>
      <div class="w3-row" style="text-align: justify;">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Decimal and Hexadecimal Numbers</h1>
            <p>The decimal numbers have base 10 and they include 0, 1, 2, 3, 4, 5, 6, 7, 8, 9. The hexadecimal numbers have base 16 and they are counted as the modern version of binary numbers. The conversion of these numbers is also easy. Find the process below.</p>
        </div>
      </div>
      <div class="w3-row" style="text-align: justify;">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Conversion</h1>
            <p>The decimal to hex conversion is really simple, you can also take help of our tool to find out the correct answer. First, divide the given decimal number by 16. Get the number quotient. Get the reminder for the further hex digits. Keep on looping these steps until you get quotient to 0.</p>
        <br>
      </div>
      </div>
      <footer-app></footer-app>
  </div>
</div>
</template>

<script>
import footer from '~/components/footer.vue';
import { BigNumber } from 'bignumber.js';

export default {

  meta: {
  // sets document title
  title: 'Decimal to Hexadecimal Converter | Dec to Hex Translator Online',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: {
    description: { name: 'description', content: 'Best decimal to hexadecimal converter. Get the answers about the conversions and learn how to convert decimal number to a hexadecimal.' },
    equiv: { 'http-equiv': 'Content-Type', content: 'text/html; charset=UTF-8' }
  },
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/decimal-to-hexadecimal/'}
  ]
  },
  components:{
    'footer-app': footer
  },
  data () {
    return {
      text_value: null,
            ans: ""
    }
  },
  methods: {
    dectohex() {
    var x = new BigNumber(this.text_value, 10)
    var dectobin = x.toString(16).toUpperCase ();
    this.ans = dectobin;
            },
    hextodec() {
    var x = new BigNumber(this.text_value, 16)
    var dectobin = x.toString(10);
    this.ans = dectobin;
     },
   reset() {
     this.ans = '',
     this.text_value= null
   },
  }
}
</script>

<style>
#box {
  background-color: lightgrey;
   width: 300px;
   border: 5px solid gray;
   padding: 10%;
   margin-left: 30%;

}
</style>
