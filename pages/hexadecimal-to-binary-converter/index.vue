<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Hexadecimal to Binary</h1>
          <Adsense
        class="adsbygoogle"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense><br><br>
          <p>Use this hexadecimal to binary converter to convert any base-16 hex number into the zeros and ones. Enter a hex number value into the box and convert that hex number into the correct binary number with ease. Hex numbers contain 0-9 in numbers and A-z in letters. Just for an example, enter "4444" into the text area and click on the convert button, you will get the "100010001000100" answer in the conversion box.</p><br>
          <div class="w3-hover-shadow w3-panel w3-leftbar w3-light-grey" style="height: 323px;"><br>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" v-on:click="hextobin()" style="width: 49%">Hexadecimal to binary</button>
          <button class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" v-on:click="reset()" style="width: 49%">clear all the fields</button><br><br>
            <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">Conversion: {{ ans }}</p>
          </div>
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
          <router-link to="/decimal-to-binary/">
          <li>Decimal to Binary</li>
        </router-link>
        <router-link to="/binary-to-decimal/">
        <li>Binary to Decimal</li>
      </router-link>
            <router-link to="/decimal-to-hexadecimal/">
            <li>Decimal to Hexadecimal</li></router-link>
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
          <h1 class="w3-text-teal">How to Convert Hexadecimal to Binary?</h1>
          <article>
            Converting hexadecimal to binary numbers is not that difficult task. Hex numbers are used to showcase the binary numbers most shortly. Binary number is the base 2 while hex numbers are the bast - 16. First, get the decimal number equivalent of that hexadecimal number from the table and you are done. You will get the binary number equivalent to the hex number.
          </article><br>
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
  head() {
  // sets document title
  return {
  title: 'Hex to binary converter | convert base 16 to zeros and ones',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Convert hexadecimal to binary numbers with this tool. Enter a hex number and get the equivalent base 2 number easily with this amazing tool.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/hexadecimal-to-binary-converter/'}
  ]
  }
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
    bintohex() {
      var bin = this.text_value;
      var m = new  BigNumber(bin, 2)
      var binn = m.toString(16);
      this.ans = binn;
            },
    hextobin() {
      var hex = this.text_value;
      var x = new BigNumber(hex, 16);
      var dect = x.toString(2);
      this.ans = dect;
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
table, th, td {
  border: 1px solid black;
}
</style>
