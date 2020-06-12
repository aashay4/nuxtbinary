<template>
  <div>
    <div class="w3-main" style="margin-left:250px"><br><br>
    <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Convert 3 in Binary</h1>
<div class="w3-hover-shadow w3-panel w3-leftbar w3-light-grey" style="height: 376px;"><br>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button v-on:click="dectobin()" class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" style="display: inline-block">In Binary</button>
          <button v-on:click="reset()" class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" style="display: inline-block">Reset</button><br><br>
            <div class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; height: 110px; overflow: scroll;"><b>Conversion:</b> {{ ans }}</div><br><br>
          </div>
          <p>Here is 3 in binary : 11</p>
        </div><br>
        <div class="w3-third w3-container">
          <h3 style="background-color: silver;">Other Useful Tools</h3>
          <ul>
            <router-link to="/ascii-to-binary">
            <li>ASCII to Binary</li>
          </router-link>
          <router-link to="/decimal-to-binary">
            <li>
              Decimal to Binary
            </li>
          </router-link>
          <router-link to="/hexadecimal-to-binary-converter">
            <li>
              Hexadecimal to Binary Translator
            </li>
          </router-link>
            <router-link to="/binary-to-hexadecimal">
            <li>Binary to Hexadecimal</li></router-link>
            <router-link to="/decimal-to-hexadecimal">
            <li>Decimal to Hexadecimal</li></router-link>
            <router-link to="/decimal-to-octal">
            <li>Decimal to Octal</li></router-link>
            <router-link to="/binary-to-octal">
            <li>Binary to Octal</li></router-link>
            <router-link to="/hexadecimal-to-octal">
            <li>Hexadecimal to Octal</li></router-link>
            <router-link to="/qr-code-generator">
            <li>QR Code Generator</li></router-link>
            <router-link to="/qr-code-reader">
            <li>QR Code Reader</li></router-link>
            <router-link to="/binary-converter">
            <li>Binary Converter</li></router-link>
          </ul><br><br>
          <h3 style="background-color: silver;">Useful Resources</h3>
          <ul>
            <router-link to="/about-creator">
            <li>About</li>
          </router-link>
            <router-link to="/blog">
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
import { BigNumber } from 'bignumber.js';

export default {
  head() {
  // sets document title
  return {
  title: 'How to Write 3 in binary?',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: '' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/3-in-binary/'}
  ]
  }
  },
  components:{
    'footer-app': footer
  },
  data () {
    return {
      text_value: 3,
            ans: '11',
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
</style>
