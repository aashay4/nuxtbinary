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
          <h1 class="w3-text-teal">Decimal to Binary Converter</h1>
          <Adsense
        class="adsbygoogle"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense><br><br>
          <p>To use this decimal to binary tool, enter a decimal number up to 19 characters and click on the conversion button. For example, enter a decimal number "44" into the text box and click on the button, you will get the binary number "101100". If you want to convert a binary number into the decimal then enter zeros and ones into the box and click on specific converter button. With this decimal to binary tool you will also be able to get the correct conversion for oct and hex numbers.</p>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button v-on:click="dectobin(); dectohex(); dectooct();" style="width: 49%">Decimal to Binary</button>
          <button v-on:click="reset()" style="width: 49%">clear all the fields</button><br><br>
            <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">Conversion: {{ ans }}</p>
            <h3><b>{{ text_value }} to base-8</b></h3>
            <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">Conversion: {{ ansoct }}</p>
            <h3><b>{{ text_value }} to base-16</b></h3>
            <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">Conversion: {{ anshex }}</p>
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
          <h2 class="w3-text-teal">Decimal Numbers</h2>
          <p>The Decimal numbers are nothing but zero and set of other counting numbers. In the number system, all the digits are placed to the left and right of the decimal point. All the decimal points let us know where the place of a specific number is.</p>
        </div>
      </div>
      <div class="w3-row" style="text-align: justify;">
        <div class="w3-twothird w3-container">
          <h2 class="w3-text-teal">The Decimal to Binary Converter Structure</h2>
            <p>Just for an example, if you want to convert decimal to binary number then follow these steps. Firstly, divide the given number by 2. After you are dividing it by 2, get the float for the next iteration. Note the reminder for the binary digit. For example, if you enter the number "4422" in the textbox and you will get this answer: 1000101000110.</p><br>
        </div>
        </div>
      <div class="w3-row" style="text-align: justify;">
        <div class="w3-twothird w3-container">
          <h2 class="w3-text-teal">Conversion of 12 to Binary</h2>
            <p>Converting 12 decimal to binary is pretty simple. Firstly, divide 12 by 2 and the remainder would be 0 and quotient for 12 will be 6. Again dividing 6 by two will give 0 remainder and 3 quotients. Now, dividing 3 by 2 will give the remainder of 1 and quotient of 1. That's it! The decimal to binary conversion of number 12 will be 1100.</p><br>
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
  title: 'Decimal to Binary Online Converter | Convert Numbers with this tool',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'With Decimal to Binary converter, get the numbers converted really easily. Get to know about the conversion process of binary to decimal and vice a versa.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/decimal-to-binary/'}
  ]
  }
  },
  components:{
    'footer-app': footer
  },
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

<style scoped>
#box {
  background-color: lightgrey;
   width: 300px;
   border: 5px solid gray;
   padding: 10%;
   margin-left: 30%;

}
</style>
