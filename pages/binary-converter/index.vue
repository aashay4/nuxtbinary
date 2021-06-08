<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Binary Converter</h1>
          <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense>
          <p>Full Binary converter, Enter a binary value and click on the button. You will get from binary to hex, dec, oct and text values.</p>
            <div>
            <binarytranslator />
          </div>
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
            <router-link to="/decimal-to-hexadecimal/">
            <li>Decimal to Hexadecimal</li></router-link>
            <router-link to="/decimal-to-octal/">
            <li>Decimal to Octal</li></router-link>
            <router-link to="/octal-to-binary/">
            <li>Octal to Binary Converter</li></router-link>
              <router-link to="/hexadecimal-to-binary-converter/">
              <li>Hexadecimal to Binary Converter</li></router-link>
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
          <h1 class="w3-text-teal">How to Use this Binary Converter?</h1>
            <p>To use this 01100010 01101001 01101110 01100001 01110010 01111001 converter, just enter the binary numbers in the box above and click on the convert button, you will get the answers for the given number in just a few seconds. The number entered by you will be converted into dec, oct, hex, and text values. If the numbers cannot be converted then you will receive a message for the same.</p>
        </div>
      </div>
      <footer-app></footer-app>
  </div>
</div>
</template>

<script>
import footer from '~/components/footer.vue';
import binarytranslator from '~/components/binarytranslator.vue';

export default {

  head() {
  // sets document title
  return {
  title: 'Binary Converter, Convert from binary to dec, hex, oct and text values.',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: '' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/binary-converter/'}
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

<style scoped>
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
</style>
