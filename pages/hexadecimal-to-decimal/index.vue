<template>
  <div>
    <div class="w3-main" style="margin-left:250px"><br>
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Hexadecimal to Decimal</h1>
          <Adsense
        class="adsbygoogle"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense><br><br>
          <p>Convert hexadecimal to decimal easily with our tool. Enter any hexadecimal number in the box, click on the button and get the decimal conversion with ease. For example, enter a hexadecimal number "24" in the box, click on the "Hexadecimal to decimal" button and you will get the answer "36".</p><br>
          <div class="w3-hover-shadow w3-panel w3-leftbar w3-light-grey" style="height: 500px;"><br>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" v-on:click="hextodec(); hextobin();" style="width: 49%">Hexadecimal to Decimal</button>
          <button class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" v-on:click="reset()" style="width: 49%">clear all the fields</button><br><br>
          <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">Conversion: {{ ans }}</p>
          <h3><b>({{ text_value }}) to binary</b></h3>
          <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll"><b>Conversion:</b> {{ ansbin }}</p>
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
          <h1 class="w3-text-teal">How to convert hexadecimal to decimal?</h1>
          <p>The conversion of any number into a hex number is simple. The regular hex number is the sum of digits multiplied with the power of 16. For example, if you have the number "AE88" then convert the character "A" & "E" into their equivalent decimal value. After converting, you will get an answer of "44680".</p>
          <h2 class="w3-text-teal">About Hex & Decimal Numbers</h2>
          <p>Hexadecimal numbers are the base-16 numbers. It includes o, 1, 2, 3, 4, 5, 6, 7, 8, 9, and A to F letters. It groups the binary numbers which are built with zeros and ones in sets of four different digits. Hexadecimal is used in MAC address, computer programming, and many other modern microprocessors. While decimal numbers contain just 0 to 9. This is also one of the most important numbering systems and is used by a lot of modern microprocessors.</p>
          <h2 class="w3-text-teal">Importance of Hexadecimal to Decimal Conversion</h2>
          <p>Hexadecimal is useful for writing large binary & decimal numbers in just a few digits. As binary contains just zeros & ones and decimal numbers contain 0 to 9 numbers, it becomes difficult to read large numbers for humans. For that reason, it is important to convert hexadecimal to decimal to hexadecimal for a better understanding of this system.</p>
          <h2 class="w3-text-teal">Hexadecimal to decimal Conversion Table</h2>
          <table style="width:25%">
            <tbody>
  <tr>
    <th>Hex</th>
    <th>Decimal</th>
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
    <td>8</td>
  </tr>
  <tr>
    <td>9</td>
    <td>9</td>
  </tr>
  <tr>
    <td>A</td>
    <td>10</td>
  </tr>
  <tr>
    <td>B</td>
    <td>11</td>
  </tr>
  <tr>
    <td>C</td>
    <td>12</td>
  </tr>
  <tr>
    <td>D</td>
    <td>13</td>
  </tr>
  <tr>
    <td>E</td>
    <td>14</td>
  </tr>
  <tr>
    <td>F</td>
    <td>15</td>
  </tr>
  <tr>
    <td>10</td>
    <td>16</td>
  </tr>
  <tr>
    <td>11</td>
    <td>17</td>
  </tr>
  <tr>
    <td>12</td>
    <td>18</td>
  </tr>
  <tr>
    <td>13</td>
    <td>19</td>
  </tr>
  <tr>
    <td>14</td>
    <td>20</td>
  </tr>
  <tr>
    <td>15</td>
    <td>21</td>
  </tr>
  <tr>
    <td>16</td>
    <td>22</td>
  </tr>
  <tr>
    <td>17</td>
    <td>23</td>
  </tr>
  <tr>
    <td>18</td>
    <td>24</td>
  </tr>
  <tr>
    <td>19</td>
    <td>25</td>
  </tr>
  <tr>
    <td>20</td>
    <td>32</td>
  </tr>
  <tr>
    <td>21</td>
    <td>33</td>
  </tr>
  <tr>
    <td>22</td>
    <td>34</td>
  </tr>
  <tr>
    <td>23</td>
    <td>35</td>
  </tr>
  <tr>
    <td>24</td>
    <td>36</td>
  </tr>
  <tr>
    <td>25</td>
    <td>37</td>
  </tr>
</tbody>
</table>
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
  head() {
  // sets document title
  return {
  title: 'Hexadecimal to Decimal Converter | Hex to Decimal online',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'This hexadecimal to decimal converter helps you to convert base-16 numbers to base-10 numbers with the help of a hex to decimal conversion chart.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/hexadecimal-to-decimal/'}
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
            ansbin: ''
    }
  },
  methods: {
    hextobin() {
      var hex = this.text_value;
      var x = new BigNumber(hex, 16);
      var dect = x.toString(2);
      this.ansbin = dect;
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
table, th, td {
  border: 1px solid black;
}
</style>
