<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Convert Binary to Hexadecimal</h1>
          <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense>
          <p>To use this binary to hex converter, enter the binary number into this text field and click on the button, "Binary to Hexadecimal", you will get the answer for the equivalent hexadecimal number of the binary number. Enter the value "101011111" in the box and you will get the answer of "15F" as the answer.</p>
          <div class="w3-hover-shadow w3-panel w3-leftbar w3-light-grey" style="height: 400px;"><br><br>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" v-on:click="bintohex()">Binary to Hexadecimal</button>
          <button class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" v-on:click="hextobin()">Hexadecimal to Binary</button>
          <button class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" v-on:click="reset()">Reset Fields</button><br><br>
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
          <h1 class="w3-text-teal">Hexadecimal Numbers</h1>
          <p>The hexadecimal is a base-16 numbering system. The hexadecimal numbers are nothing but 0-9 and then use A to F. The conversion of binary to hex numbers is simple. You can either use our tool or perform the conversion operation by yourself.</p><br>
          <p>The hexadecimal numbers are the modern way to show binary numbers to computer systems. When showing the content from computer storage, one hexadecimal number can show the representation of four various binary numbers. Two hexadecimal numbers can represent eight binary digits and so on.</p><br>
          <p>You can have a look at different values of hex numbers along with zeros and one in the table below!</p>
          <h2 class="w3-text-teal">How to convert binary to hexadecimal?</h2>
          <article>
            As we all know, binary numbers are only zeros and ones, and no other number can be placed in the place of these numbers. Where hexadecimal numbers contain either 0-9 numbers or A-F letters. Apart from that, hexadecimal is base - 16, it possible to convert binary to hex number but the only condition required is you need at least four base-2 numbers to make any kind of conversion. To convert binary to hexadecimal, you need to the binary into group of 4 and process those four numbers to get desired the result. You can also use our tool to get an accurate answer.
          </article><br>
          <table style="width:25%">
            <tbody>
  <tr>
    <th>Hex</th>
    <th>Binary</th>
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
    <td>10</td>
  </tr>
  <tr>
    <td>3</td>
    <td>11</td>
  </tr>
  <tr>
    <td>4</td>
    <td>100</td>
  </tr>
  <tr>
    <td>5</td>
    <td>101</td>
  </tr>
  <tr>
    <td>6</td>
    <td>110</td>
  </tr>
  <tr>
    <td>7</td>
    <td>111</td>
  </tr>
  <tr>
    <td>8</td>
    <td>1000</td>
  </tr>
  <tr>
    <td>9</td>
    <td>1001</td>
  </tr>
  <tr>
    <td>A</td>
    <td>1010</td>
  </tr>
  <tr>
    <td>B</td>
    <td>1011</td>
  </tr>
   <tr>
    <td>C</td>
    <td>1100</td>
  </tr>
  <tr>
    <td>D</td>
    <td>1101</td>
  </tr>
  <tr>
    <td>E</td>
    <td>1110</td>
  </tr>
  <tr>
    <td>F</td>
    <td>1111</td>
  </tr>
  <tr>
    <td>10</td>
    <td>10000</td>
  </tr>
  <tr>
    <td>20</td>
    <td>100000</td>
  </tr>
   <tr>
    <td>40</td>
    <td>1000000</td>
  </tr>
  <tr>
    <td>80</td>
    <td>10000000</td>
  </tr>
  <tr>
    <td>100</td>
    <td>100000000</td>
  </tr>
  </tbody>
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
  title: 'Binary to Hexadecimal Converter | Convert binary to hex',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Binary to hex converter. The simplest online translator of binary to hexadecimal conversions. Visit here and get answers!' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/binary-to-hexadecimal/'}
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
      var binn = m.toString(16).toUpperCase();
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
   }
  }
}
</script>

<style>
@media (min-width: 350px) {
    .infeed {
      height: 240px;
    }
  }
 @media (min-width: 500px) {
    .infeed {
      height: 200px;
    }
  }
 @media (min-width: 800px) {
    .infeed {
      height: 290px;
    }
  }
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
