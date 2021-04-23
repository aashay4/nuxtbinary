<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <Adsense
      class="adsbygoogle infeed"
      style="display:block"
      data-ad-client="ca-pub-6829148792481216"
      data-ad-slot="1665700659"
      data-ad-format="auto"
      data-full-width-responsive="true">
      </Adsense>
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Decimal to Binary Converter</h1>
          <Adsense
        class="adsbygoogle infeed"
        style="display:block"
        data-ad-client="ca-pub-6829148792481216"
        data-ad-slot="1416243045"
        data-ad-format="auto"
        data-full-width-responsive="true">
        </Adsense><br><br>
          <paradecimal /><br>
          <dectobinary />
        </div><br>
        <othertoolsdecimaltobinary />
      </div>
      <decimalcontent />
        <footer-app></footer-app>
  </div>
</div>
</template>

<script>
import decimalcontent from '~/components/decimalcontent.vue';
import othertoolsdecimaltobinary from '~/components/othertoolsdecimaltobinary.vue';
import paradecimal from '~/components/para-decimal.vue';
import dectobinary from '~/components/dectobinary.vue';
import footer from '~/components/footer.vue';

export default {

  head() {
  // sets document title
  return {
  title: 'Decimal to Binary Calculator (Decimal Converter)',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Decimal to binary converter.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/decimal-to-binary/'}
  ]
  }
  },
  components:{
    'footer-app': footer,
    'dectobinary': dectobinary,
    'paradecimal': paradecimal,
    'othertoolsdecimaltobinary': othertoolsdecimaltobinary,
    'decimalcontent': decimalcontent
  },
  data () {
    return {
      text_value: null,
            ans: "",
            anshex: '',
            ansoct: ''
    }
  },
  methods: {

  }
}
</script>

<style>
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
table, th, td {
  border: 1px solid black;
}
</style>
