<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Octal to Binary Converter</h1>
          <Adsense
        class="adsbygoogle adslot_1"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense><br><br>

          <p>Looking for octal to Binary conversion in the least amount of time? Enter the octal number below and click on the conversion button to get the conversion of an octal number into the binary number. Enter numbers like 16, 32, or 64 here and find out the equivalent binary values of these numbers. In the same way, you can enter zeros and ones to find out the octal values of those numbers.</p>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button v-on:click="octtobin()" style="width: 49%">Octal to binary</button>
          <button v-on:click="reset()" style="width: 49%">clear all the fields</button><br><br>
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
            <h1 class="w3-text-teal">Octal Number</h1>
            <p>Oct numbers have the base 8. It is easy to convert any number(decimals, binary or hexadecimal) into the oct numbers. Please find the conversion of oct into zeros and ones. You can also use our tool if you are looking for an online conversion tool, it is free.</p>
            <h2 class="w3-text-teal">Octal to Binary Conversion</h2>
            <p>The octal to binary conversion takes place in four different parts. The first part is separating each octal number. Once you separate the octal numbers, find the equivalent binary numbers for those octal numbers. Do note, if you find any binary number shorter than 3 bits then do add zeros in the particular number. Write down all the binary numbers together and you will get the equivalent binary number to that octal number. To find the binary of octal, you can use our tool to get the accurate numbers totally for free.</p>
            <p><table style="width:25%">
    <tr>
      <th>Oct</th>
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
      <td>10</td>
      <td>1000</td>
    </tr>
    <tr>
      <td>11</td>
      <td>1001</td>
    </tr>
    <tr>
      <td>12</td>
      <td>1010</td>
    </tr>
    <tr>
      <td>13</td>
      <td>1011</td>
    </tr>
     <tr>
      <td>14</td>
      <td>1100</td>
    </tr>
    <tr>
     <td>15</td>
     <td>1101</td>
   </tr>
   <tr>
    <td>20</td>
    <td>10000</td>
  </tr>
  <tr>
   <td>40</td>
   <td>100000</td>
 </tr>
 <tr>
  <td>100</td>
  <td>1000000</td>
</tr>
<tr>
 <td>1000</td>
 <td>1000000000</td>
</tr>
<tr>
 <td>2000</td>
 <td>10000000000</td>
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

export default {

  head() {
  // sets document title
  return {
  title: 'Octal to binary converter | Best Online Tool for octal Conversion',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Convert octal to binary number with the help of this free tool.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/octal-to-binary-converter/'}
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
    octtobin() {
      this.aaa = parseInt(this.text_value);
      var octtobin = (parseInt(this.aaa, 8).toString(2));
      this.ans = octtobin;
     },
   reset() {
     this.ans = '',
     this.text_value= null
   },
  }
}
</script>

<style scoped>
.adslot_1 { display:inline-block; width: 320px; height: 50px; }
@media (max-width: 400px) { .adslot_1 { display: none; } }
@media (min-width:500px) { .adslot_1 { width: 468px; height: 60px; } }
@media (min-width:800px) { .adslot_1 { width: 728px; height: 90px; } }
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
