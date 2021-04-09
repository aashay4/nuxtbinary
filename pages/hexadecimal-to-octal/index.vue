<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Hexadecimal to Octal</h1>

          <Adsense
        class="adsbygoogle"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense><br><br>
          <p>Convert Hex to octal with the help of this tool. Enter any hexadecimal value into the input box, click on the conversion button and get the answer to your desired number. Enter a hex number "16" and click on the button, you will find out the correct answer in the conversion box. In the same way, you can also convert an octal number into a hex number with this tool.</p>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button v-on:click="hextooct()" style="width: 32%">Hexadecimal to Octal</button>
          <button v-on:click="octtohex()" style="width: 32%">Octal to Hexadecimal</button>
          <button v-on:click="reset()" style="width: 33%">clear all the fields</button><br><br>
            <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">Conversion: {{ ans }}</p>
        </div><br>
        <div class="w3-third w3-container">
          <h3 style="background-color: silver;">Other Useful Tools</h3>
          <ul>
            <router-link to="/ascii-to-binary/">
            <li>ASCII to Binary</li>
          </router-link>
          <router-link to="/decimal-to-binary/">
            <li>
              Decimal to Binary
            </li>
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
          <table style="width:25%">
  <tr>
    <th>Hex</th>
    <th>Octal</th>
  </tr>
  <tr>
    <td>0</td>
    <td>0</td>
  </tr>
  <tr>
    <td>1</td>
    <td>1</td>
  </tr>
  <tr>
    <td>2</td>
    <td>2</td>
  </tr>
  <tr>
    <td>3</td>
    <td>3</td>
  </tr>
  <tr>
    <td>4</td>
    <td>4</td>
  </tr>
  <tr>
    <td>5</td>
    <td>5</td>
  </tr>
  <tr>
    <td>6</td>
    <td>6</td>
  </tr>
  <tr>
    <td>7</td>
    <td>7</td>
  </tr>
  <tr>
    <td>8</td>
    <td>10</td>
  </tr>
  <tr>
    <td>9</td>
    <td>11</td>
  </tr>
  <tr>
    <td>A</td>
    <td>12</td>
  </tr>
  <tr>
    <td>B</td>
    <td>13</td>
  </tr>
   <tr>
    <td>C</td>
    <td>14</td>
  </tr>
  <tr>
    <td>D</td>
    <td>15</td>
  </tr>
  <tr>
    <td>E</td>
    <td>16</td>
  </tr>
  <tr>
    <td>F</td>
    <td>17</td>
  </tr>
  <tr>
    <td>10</td>
    <td>20</td>
  </tr>
  <tr>
    <td>20</td>
    <td>40</td>
  </tr>
   <tr>
    <td>40</td>
    <td>100</td>
  </tr>
  <tr>
    <td>80</td>
    <td>200</td>
  </tr>
  <tr>
    <td>100</td>
    <td>400</td>
  </tr>
</table><br>
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
  title: 'Hexadecimal to Octal | Tool for Base 16 to 8 Number',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Convert hexadecimal to octal numbers very easily with the help of our number converter. You can also convert octal to the hex numbers.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/hexadecimal-to-octal/'}
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
            isHidden: true
    }
  },
  methods: {
    hextooct() {
      var x = new BigNumber(this.text_value, 16);
      var hextooct = x.toString(8).toUpperCase ();
      this.ans = hextooct;
            },
    octtohex() {
      var y = new BigNumber(this.text_value, 8);
      var octtohex = y.toString(16).toUpperCase ();
      this.ans = octtohex;
     },
   reset() {
     this.ans = '',
     this.text_value= null
   },
   activate() {
    setTimeout(() => this.isHidden = false, 10000);
  }
 },
 beforeMount(){
  this.activate()
},

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
