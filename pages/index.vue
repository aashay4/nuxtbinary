<template>
  <div>
    <div class="w3-main" style="margin-left:250px"><br>
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
          <h1 class="w3-text-teal">Binary To Text Converter (Translator)</h1><br>
          <iframe src="//rcm-na.amazon-adsystem.com/e/cm?o=1&p=8&l=ez&f=ifr&linkID=5dd3978213e873fd0f5c1376fe28a3de&t=aasshey-20&tracking_id=aasshey-20" width="120" height="240" scrolling="no" border="0" marginwidth="0" style="border:none;" frameborder="0"></iframe><br>
          <p>To use the binary to text tool, enter a binary number into the box, click on the binary translator button and get the equivalent text into the output. For example, insert “01000011 01101111 01101110 01110110 01100101 01110010 01110100” into the box and click on the binary to text button, you will get the text string “Convert”.
If you want to convert text to binary, then enter any text into the text box and click on the button “Text to binary”. You will get the equivalent binary value with our binary translator.<br><br>
</p>
<div class="w3-hover-shadow w3-panel w3-leftbar w3-light-grey" style="height: 376px;"><br>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button v-on:click="binarytotext()" class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" style="display: inline-block">Binary to Text</button>
          <button v-on:click="texttobinary()" class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" style="display: inline-block">Text to Binary</button>
          <button v-on:click="reset()" class="w3-button w3-border w3-teal w3-padding-large w3-hover-gray" style="display: inline-block">Reset</button><br><br>
          <div class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; height: 110px; overflow: scroll;"><b>Conversion:</b> {{ ans }}</div><br><br>
          </div>
          <Adsense
        class="adsbygoogle"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense>
            <h1 class="w3-text-teal">Binary Translator</h1>
            <div>
              <p>Want to convert dec, hex or oct to the equivalent binary number? Here is the full binary translator. Please find it below. Enter any binary number in the box and click of the conversion, you will find out the conversion of that binary number into its equivalent hex, dec or octal number in just a second with our binary translator.</p>
            <binarytranslator />
          </div>
        </div><br>
        <div class="w3-third w3-container">
          <h3 style="background-color: silver;">Other Useful Tools</h3>
          <ul>
            <a href="/ascii-to-binary/">
            <li>ASCII to Binary</li>
          </a>
          <a href="/hexadecimal-to-decimal/">
          <li>Hexadecimal to Decimal</li>
        </a>
          <a href="/decimal-to-binary/">
            <li>
              Decimal to Binary
            </li>
          </a>
          <a href="/hexadecimal-to-binary-converter/">
            <li>
              Hexadecimal to Binary Translator
            </li>
          </a>
            <a href="/binary-to-hexadecimal/">
            <li>Binary to Hexadecimal</li></a>
            <a href="/decimal-to-hexadecimal/">
            <li>Decimal to Hexadecimal</li></a>
            <a href="/decimal-to-octal/">
            <li>Decimal to Octal</li></a>
            <a href="/binary-to-octal/">
            <li>Binary to Octal</li></a>
            <a href="/hexadecimal-to-octal/">
            <li>Hexadecimal to Octal</li></a>
            <a href="/qr-code-generator/">
            <li>QR Code Generator</li></a>
            <a href="/qr-code-reader/">
            <li>QR Code Reader</li></a>
            <a href="/binary-converter/">
            <li>Binary Converter</li></a>
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
          <h1 class="w3-text-teal">Binary</h1>
            <p>Binary is just a number system that uses only two digits, o and 1 to rectify different queries. This number system one of the most popular systems in modern computer processing, electronics, wireless networking systems, data process over a network layer. A computer system can only understand the binary numbers and for that reason, it has become one of the most popular terms in the digital world. You can use this binary translator for the binary to text conversion.</p>
        </div>
      </div>

      <div class="w3-row w3-padding-64" style="text-align: justify;">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">How to convert Binary to Text?</h1>
          <p>For example, if you want to convert a binary number "01000001" into its equivalent text number. Take the first eight characters binary given to you(That's probably 01000001) and convert it into the ASCII values. Now find out the ASCII value of the specific character. And you will get the number "A" for that binary number. If you have been given number (0100000101010111). Now take the first eight characters, find the equivalent text number. After the completion, take another eight characters and find their relevant values. Once you have converted the values, you can take help of our binary to text tool to check out the answer of the given number.</p>
        </div>
      </div>
      <div class="w3-row w3-padding-64" style="text-align: justify;">
        <div class="w3-twothird w3-container">
          <h3 class="w3-text-teal">Convert 01000001 01001110 binary code to Text</h3>
          <p>The binary to text code conversion of 01000001 01001110 is AN. As mentioned above, take the first eight characters of the given number. So, the first eight characters of this number are 01000001. The binary to text conversion of this number is "A". Once you have converted this number, convert another number. The second set for conversion would be 01001110. Again, this is the same number and conversion would be "N". So, the final binary to text conversion of "01000001 01001110" would be "AN".</p>
        </div>
      </div>
      <footer-app></footer-app>
  </div>
</div>
</template>

<script>
import footer from '../components/footer.vue';
import binarytranslator from '../components/binarytranslator.vue';

export default {
  head() {
  // sets document title
  return {
  title: 'Binary to Text Converter (Binary translator)',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'A binary to text converter and also binary translator. Just enter a binary code and convert it into the equivalent text values with this free binary code translator. Same for text to binary conversion.' }
  ],
  link: [
 {rel: 'canonical', href: 'https://binarytotext.net/'}
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
            ans: "",
            aaa: null,
            livePaper: false
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
    binarytotext() {
        var bintext, textresult="", binlength;
        this.aaa = this.text_value;
        bintext = this.aaa.replace(/[^01]/g, "");
			binlength = bintext.length-(bintext.length%8);
			for(var z=0; z<binlength; z=z+8) {
				textresult += String.fromCharCode(parseInt(bintext.substr(z,8),2));
                                this.ans = textresult;
        }
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
