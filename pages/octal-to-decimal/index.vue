<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Octal to Decimal</h1>
          <Adsense
        class="adsbygoogle"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense><br><br>

          <p>To get the conversion of decimal to octal, enter a value below and click on the button. Enter a decimal value "4444" and you will get the answer of "10534". Same way, you can also get an answer from the octal number to the decimal number. Enter the same number in the box and you will get the equivalent decimal conversion.</p>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button v-on:click="octtodec()" style="width: 49%">Octal to Decimal</button>
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
            <li>Decimal to Hexadecimal</li></router-link>
            <router-link to="/decimal-to-octal/">
            <li>Decimal to Octal</li>
            </router-link>
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
          <h1 class="w3-text-teal">Octal Numbers</h1>
            <p>The oct is a short form for the octal numbers. It is the base-8 numbering system that uses digital from 0 to 7. In the octal numbering system, each place is the power of eight. The biggest benefit of octal numbers is nothing but they can directly be converted into the binary number in the simplest manner. Even the decimal to octal conversion is also really simple, find the conversion technique below.</p>
        </div>
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Octal to decimal conversion</h1>
              <p>The normal decimal number is nothing but the sum of numbers multiplied by 10 raise to X(Where x is any given decimal number). For example, if you want to convert 37 octal number into decimal then the calculation would be as shown below,</p>
              <p><b>37 = (3*8) + (7*1) = 31</b></p>
                <p>You can also use our tool to perform a similar conversion.</p>
                <p>
                  <table style="width:25%">
          <tr>
            <th>Base 8</th>
            <th>Base 10</th>
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
            <td>10</td>
            <td>8</td>
          </tr>
          <tr>
            <td>11</td>
            <td>9</td>
          </tr>
          <tr>
            <td>12</td>
            <td>10</td>
          </tr>
          <tr>
            <td>13</td>
            <td>11</td>
          </tr>
          <tr>
            <td>14</td>
            <td>12</td>
          </tr>
          <tr>
            <td>15</td>
            <td>13</td>
          </tr>
          <tr>
            <td>24</td>
            <td>20</td>
          </tr>
          <tr>
            <td>32</td>
            <td>26</td>
          </tr>
          <tr>
            <td>40</td>
            <td>32</td>
          </tr>
          <tr>
            <td>64</td>
            <td>52</td>
          </tr>
          <tr>
            <td>72</td>
            <td>58</td>
          </tr>
          <tr>
            <td>100</td>
            <td>64</td>
          </tr>
        </table>
                </p>
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
  title: 'An online Octal to Decimal Converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Enter an octal base 8 number in the box and convert it into the decimal number with this octal to decimal translator.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/octal-to-decimal/'}
  ]
  }
  },
  components:{
    'footer-app': footer
  },
  data () {
    return {
      text_value: null,
            total: null,
            ans: "",
            aaa: null,
            text_val: null
    }
  },
  methods: {
    dectooct() {
    var x = new BigNumber(this.text_value, 10)
    var dectobin = x.toString(8);
    this.ans = dectobin;
            },
    octtodec() {
    var x = new BigNumber(this.text_value, 8)
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

<style scoped>
#box {
  background-color: lightgrey;
   width: 300px;
   border: 5px solid gray;
   padding: 10%;
   margin-left: 30%;

}
</style>
