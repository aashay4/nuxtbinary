<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Decimal to Fraction Calculator</h1>
          <Adsense
          v-if="elementVisible === true"
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense><br><br>
          <p>Easily convert decimal to fraction with this free tool. Just enter numbers and convert them into the fraction quickly.</p><br>
          <input type="text" v-model="text_value" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/><br><br>
          <button v-on:click="dectofra()" style="width: 49%">Decimal to Fraction</button>
          <button v-on:click="reset()" style="width: 49%">clear all the fields</button><br><br>
          <div class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">
              <table>
                <tr>
                    <td>{{yyy}}</td>
                  <td>{{ ans }}</td>
                </tr>
                <tr>
                  <td class="w3-border-top">{{ans1}}</td>
                </tr>
              </table>
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
      <div class="w3-row w3-padding-64" style="text-align: justify;">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">How to convert Decimal to Fraction?</h1>
          <p>Converting the decimal values to fractions is quite simple. Let's understand it with an example. For example, if you want to convert 0.444 into the fraction then first of all remove the decimal numbering from this original number. So, after removing the decimal number, the number will look like 444/1000 or 444 divided by 100. Simplify the fraction value. So, in the first step, divide the equation by 2. You will get 222/500. In the second step, divide it with 2 again. So that equation will be 111/250. So, the final decimal to fraction conversion of the number 0.444 will be 111/250.</p>
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
  title: 'Convert Decimal to Fraction Easily - B2t Converter',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'With Decimal to fraction converter, just enter the numbers with points and convert decimal to fraction in easy steps.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/decimal-to-fraction/'}
  ]
  }
  },
  components:{
    'footer-app': footer
  },
  data () {
    return {
                elementVisible: false,
      text_value: null,
            ans: "",
            ans1: "",
            yyy: "",
            hhh: "",
            aaa: ""
    }
  },
  mounted: function () {
            setTimeout(() => { this.elementVisible = true }, 5000)
        },
  methods: {
    dectofra() {
      var gcd = function(a, b) {
  if (!b) return a;

  return gcd(b, a % b);
};
      var fraction = this.text_value;
  var len = fraction.toString().length - 2;
  var yyy = Math.floor(fraction)
  this.yyy = yyy
  var fff = Number(fraction - yyy).toFixed(10)

var denominator = Math.pow(10, len);
var numerator = fff * denominator;

  var divisor = gcd(numerator, denominator);

  numerator /= divisor;
  denominator /= divisor;
  this.ans = Math.floor(numerator)
  this.ans1 = Math.floor(denominator)
  this.hhh = yyy*denominator
  this.aaa = this.hhh+numerator
  alert(this.aaa)
            },
     reset() {
     this.ans = '',
     this.aaa = '',
     this.hhh = '',
     this.ans1 = '',
     this.text_value= null,
     this.yyy = ''
   },
  }
}
</script>

<style scoped>
@media (min-width: 350px) {
    .infeed {
      height: 180px;
    }
  }
 @media (min-width: 500px) {
    .infeed {
      height: 130px;
    }
  }
 @media (min-width: 800px) {
    .infeed {
      height: 200px;
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
