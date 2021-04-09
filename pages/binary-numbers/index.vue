<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
    <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Binary numbers</h1>
          <Adsense
        class="adsbygoogle"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense><br><br>
        <p>Binary numbers consist of just zeros and ones are used by a huge number of electronic devices and computer systems. Since binary numbers just include zeros and ones, it is really easy for the computer systems to process them. Along with that, these numbers are also the fastest among the other numbers. For that reason, it is used by a huge number of motherboards and systems. Not only that, but binary numbers are also used in the electronic logic gates like ADN, OR, NAND, NOR, and many others.</p><br><p>Since binary numbers consist of just zeros and ones, it is really difficult for humans to read these numbers. So, computer systems first convert the text values in the binary, and then when it is ready with the response, it converts binary to text and shows it to the users. Along with that, binary numbers occupy a lot of space on the device since the numbers are too long and eventually it ends up occupying a lot of space on the device.</p>
        <h2 class="w3-text-teal">Numbers to Binary Numbers Conversion</h2>
        <p>Just enter decimal numbers in the box, click on the convert button, and get these numbers converted into the equivalent binary numbers in the least amount of time.</p>
          <binarytranslator />
          <table style="width:25%">
  <tr>
    <th>Simple Number</th>
    <th>Binary Number</th>
  </tr>
  <tr>
    <td>8</td>
    <td>1000</td>
  </tr>
  <tr>
    <td>1</td>
    <td>1</td>
  </tr>
  <tr>
    <td>16</td>
    <td>10000</td>
  </tr>
  <tr>
    <td>12</td>
    <td>1100</td>
  </tr>
  <tr>
    <td>100</td>
    <td>1100100</td>
  </tr>
  <tr>
    <td>5</td>
    <td>101</td>
  </tr>
  <tr>
    <td>7</td>
    <td>111</td>
  </tr>
  <tr>
    <td>128</td>
    <td>10000000</td>
  </tr>
  <tr>
    <td>42</td>
    <td>101010</td>
  </tr>
  <tr>
    <td>15</td>
    <td>1111</td>
  </tr>
  <tr>
    <td>256</td>
    <td>100000000</td>
  </tr>
  <tr>
    <td>64</td>
    <td>1000000</td>
  </tr>
   <tr>
    <td>11</td>
    <td>1011</td>
  </tr>
  <tr>
    <td>9</td>
    <td>1001</td>
  </tr>
  <tr>
    <td>20</td>
    <td>10100</td>
  </tr>
  <tr>
    <td>14</td>
    <td>1110</td>
  </tr>
  <tr>
    <td>32</td>
    <td>100000</td>
  </tr>
  <tr>
    <td>25</td>
    <td>11001</td>
  </tr>
</table>
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
          <router-link to="/hexadecimal-to-binary-converter/">
            <li>
              Hexadecimal to Binary Translator
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
            <router-link to="/binary-converter/">
            <li>Binary Converter</li></router-link>
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
      <footer-app></footer-app>
  </div>
</div>
</template>

<script>
import footer from '~/components/footer.vue';
import binarytranslator from '~/components/binarytranslator.vue';
import { BigNumber } from 'bignumber.js';

export default {
  head() {
  // sets document title
  return {
  title: 'Binary numbers',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Get to know the detailed explanation about binary numbers. And also use our tool to convert different decimals into the binary numbers easily.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/binary-numbers/'}
  ]
  }
  },
  components:{
    'footer-app': footer,
    'binarytranslator': binarytranslator
  },
  data () {
    return {
      text_value: null,
            ans: '',
            aaa: null,
    }
  },
  methods: {
    dectobin() {
      var x = new BigNumber(this.text_value, 10)
    var dectobin = x.toString(2);
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
table, th, td {
  border: 1px solid black;
}
</style>
