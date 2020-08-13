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
      <h1 class="w3-text-teal">ASCII to Binary Converter</h1>
      <Adsense
    class="adsbygoogle"
    style="display:block"
    data-ad-client="ca-pub-6829148792481216"
    data-ad-slot="1416243045"
    data-ad-format="auto"
    data-full-width-responsive="true">
    </Adsense><br><br>
          <p>Enter an ASCII value or a text value into the text box and convert it into the equivalent binary number. For example, enter "Binary" in the text box or any other special character like ";" and get the text to binary conversion with our tool.</p>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button v-on:click="texttobinary()" style="width: 49%">ASCII to Binary</button>
          <button v-on:click="reset()" style="width: 49%">clear all fields</button><br><br>
          <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll"><b>Conversion:</b> {{ ans }}</p>
          <div class="w3-row" style="text-align: justify;">
              <h1 class="w3-text-teal">ASCII</h1>
              <article>ASCII is nothing but Americal standard code which is often used for the information exchanging. This is a code that represents 128 characters in the English language where each character is assigned a specific number to it. Modern computer systems use these numbers to represent text and it makes easier to transfer data from one register to the another.</article>
          </div>
          </div><br>
        <div class="w3-third w3-container">
          <h3 style="background-color: silver;">Other Useful Tools</h3>
          <ul>
            <router-link to="/">
            <li>Binary to text</li>
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

      <div class="w3-row w3-main" style="text-align: justify;">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">How to Convert ASCII to Binary?</h1>
            <p>If you want to convert the string "Text" into the binary number then follow these simple steps. Take the first character of the text(it would be "T") string and convert it into the ASCII value. And then convert the ASCII value to the equivalent binary number. The binary number for the string "T" will be 01110100. After the conversion, the number you will get should be of 8-bits, if it is less then 8-bits then add zeros and make it an 8-bits long. After the conversion of a number T, do the same conversion with other numbers, E, X, and the last one T. After completion of the operation, you will get this answer(01010100 01100101 01111000 01110100).</p>
        </div>
        <div class="w3-third w3-container">
          <p class="w3-border w3-padding-large w3-padding-32 w3-center">AD</p>
          <p class="w3-border w3-padding-large w3-padding-64 w3-center">AD</p>
        </div>
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
  title: 'ASCII text to binary zeros and ones converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Convert ASCII to binary numbers. Visit this free tool and convert text to binary in the least amount of time.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/ascii-to-binary/'}
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
            aaa: null,
    }
  },
  methods: {
    texttobinary() {

            for (var i=0; i < this.text_value.length; i++)
            {
              var e = this.text_value[i].charCodeAt(0);
              var s = "";
              do {
                var a = e % 2;
                e = (e - a) / 2;
        s = a + s;
      }while(e!=0);
        while(s.length<8) {
          if(s.length === 7) {
            s = " 0" + s;
            this.ans += s;
          }
          if(s.length === 6) {
          s = " 00" + s;
          this.ans += s;
          }
          if(s.length === 5) {
          s = " 000" + s;
          this.ans += s;
          }
          if(s.length === 4) {
          s = " 0000" + s;
          this.ans += s;
          }
          if(s.length === 3) {
          s = " 00000" + s;
          this.ans += s;
          }
        }
              }
            },
   reset() {
     this.ans = '',
     this.text_value= null
   },
  }
}
</script>

<style scoped>

</style>
