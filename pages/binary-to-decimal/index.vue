<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Convert Binary to Decimal</h1>
          <div>
          <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense>
      </div>
        <br>
          <p>You can convert binary to decimal with the help of this tool. Enter zeros and ones into the text box and get decimal digits as an output. For example, enter 101100 binary number into the box and get the "101100" answer in the other box. Same way, your inserted values will be updated into the real-time converter and you will get correct answers for the base 8 and base 16 conversions as well. Just enter any value and get started using our tool.</p><br>
          <binarydecimal />
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
        </div>
      </div>
      <div class="w3-row" style="text-align: justify;">
        <div class="w3-twothird w3-container">
            <h2 class="w3-text-teal">Binary to Decimal Conversion</h2>
            <p>If you want to convert binary to decimal, the decimal number is nothing but the sum of the given binary digits, (Xn) times the power of 2.</p><br>
              <p>
              decimal number = x0×20 + x1×21 + x2×22 + ...
            </p>
            <p>
              So, it is the conversion formula, you can also use our tool. Just enter a binary number like "10001010111000" and the answer you get will be "10001010111000".
            </p><br>
            <h2 class="w3-text-teal">Binary to Decimal Conversion Table</h2>
            <table style="width:25%">
              <tbody>
    <tr>
      <th>Binary</th>
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
      <td>10</td>
      <td>2</td>
    </tr>
    <tr>
      <td>11</td>
      <td>3</td>
    </tr>
    <tr>
      <td>100</td>
      <td>4</td>
    </tr>
    <tr>
      <td>101</td>
      <td>5</td>
    </tr>
    <tr>
      <td>110</td>
      <td>6</td>
    </tr>
    <tr>
      <td>111</td>
      <td>7</td>
    </tr>
    <tr>
      <td>1000</td>
      <td>8</td>
    </tr>
    <tr>
      <td>1001</td>
      <td>9</td>
    </tr>
    <tr>
      <td>1010</td>
      <td>10</td>
    </tr>
    <tr>
      <td>1011</td>
      <td>11</td>
    </tr>
     <tr>
      <td>1100</td>
      <td>12</td>
    </tr>
    <tr>
      <td>1101</td>
      <td>13</td>
    </tr>
    <tr>
      <td>1110</td>
      <td>14</td>
    </tr>
    <tr>
      <td>1111</td>
      <td>15</td>
    </tr>
    <tr>
      <td>10000</td>
      <td>16</td>
    </tr>
    <tr>
      <td>10001</td>
      <td>17</td>
    </tr>
     <tr>
      <td>10010</td>
      <td>18</td>
    </tr>
    <tr>
      <td>10011</td>
      <td>19</td>
    </tr>
    <tr>
      <td>10100</td>
      <td>20</td>
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
import binarydecimal from '~/components/binarydecimal.vue';
export default {

  head() {
  // sets document title
  return {
  title: 'Binary to Decimal Converter (Bin to Dec)',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Binary to decimal converter. Enter zeros and ones into the translator and get the decimal number with this bin to dec converter.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/binary-to-decimal/'}
  ]
  }
  },
  components:{
    'footer-app': footer,
    'binarydecimal': binarydecimal
  },
  data() {
    return {
      }
  },
}
</script>

<style scoped>

@media (min-width: 350px) {
    .infeed {
      height: 290px;
    }
  }
 @media (min-width: 500px) {
    .infeed {
      height: 290px;
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
