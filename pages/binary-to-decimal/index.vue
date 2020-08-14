<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <Adsense
    class="adsbygoogle"
    style="display:block"
    data-ad-client="ca-pub-6829148792481216"
    data-ad-slot="1665700659"
    data-ad-format="auto"
    data-full-width-responsive="true">
</Adsense>
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Convert Binary to Decimal</h1>
          <Adsense
        class="adsbygoogle"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense><br><br>
          <p>You can convert binary to decimal with the help of this tool. Enter zeros and ones into the text box and get decimal digits as an output. For example, enter 101100 binary number into text area and get "101100" answer in the other box. Same way, your inserted values will be updated into the real-time converter and you will get correct answers for the base 8 and base 16 conversions as well. Just enter any value and get started using our tool.</p>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button v-on:click="bintodec(); bintooct(); bintohex();" style="width: 49%">Binary to Decimal</button>
          <button v-on:click="reset()" style="width: 49%">clear all the fields</button><br><br>
            <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll"><b>Conversion:</b> {{ ans }}</p>
            <h3><b>{{ text_value }} to base-8</b></h3>
            <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll"><b>Conversion:</b> {{ ansoct }}</p>
            <h3><b>{{ text_value }} to base-16</b></h3>
            <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll"><b>Conversion:</b> {{ anshex }}</p>
        </div><br>
        <Adsense
      class="adsbygoogle"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="1416243045"
      data-ad-format="auto"
      data-full-width-responsive="true">
      </Adsense><br>
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
            <router-link to="/binary-to-hexadecimal/">
            <li>Binary to Hexadecimal</li></router-link>
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
        </div>
      </div>
      <div class="w3-row" style="text-align: justify;">
        <div class="w3-twothird w3-container">
            <b>Binary to Decimal Conversion</b>
            <p>If you want to convert binary to decimal, the decimal number is nothing but the sum of the given binary digits, (Xn) times the power of 2.<p><br>
              <p>
              decimal number = x0×20 + x1×21 + x2×22 + ...
            </p>
            <p>
              So, it is the conversion formula, you can also use our tool. Just enter a binary number like "10001010111000" and the answer you get will be "10001010111000".
            </p>
        </div>
        <div class="w3-third w3-container">
          <p class="w3-border w3-padding-large w3-padding-32 w3-center">AD</p>
          <p class="w3-border w3-padding-large w3-padding-64 w3-center">AD</p>
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
  title: 'Binary to Decimal converter | Zeros and ones to numbers translator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Best binary to decimal converter. Enter zeros and ones into the translator and get the decimal number with the help of our converter.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/binary-to-decimal/'}
  ]
  }
  },
  components:{
    'footer-app': footer,
  },
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
   },
  }
}
</script>

<style scoped>
#box {
  background-color: lightgrey;
   width: 300px;
   border: 5px solid gray;
   padding: 10%;
   margin-left: 30%;
}
</style>
