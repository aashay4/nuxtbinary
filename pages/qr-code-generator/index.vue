<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">QR Code Generator</h1>
          <p>This a real-time QR code generator and a progressive web application. Enter a website name, address, name or number into the text area. With our tool, as soon as you start typing, a QR code will be shown on the screen. You can download it and create as many QR codes as you want from our tool totally for free.</p>
          <button v-on:click="reset()" style="width: 100%">Clear all the fields</button><br><br>
          <input type="text" v-model="message" style="width: 100%" class="w3-border w3-padding-large w3-padding-32 w3-center" placeholder="Enter a value"/>
            <p class="w3-border w3-padding-large w3-padding-32 w3-right" style="width: 100%; overflow: scroll">
            <qr-code :text="message"/>
          </p>
        </div>
        <div class="w3-third w3-container">
          <p class="w3-border w3-padding-large w3-padding-32 w3-center">AD</p>
          <p class="w3-border w3-padding-large w3-padding-64 w3-center">AD</p>
        </div>

      </div>
      <div class="w3-row" style="text-align: justify;">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">What is a Qr Code?</h1>
            <p>A QR code is nothing but the machine-readable code consisting of several black and white square, mainly used to store different names, URLs and other information. A QR code can store up to 7089 digits or 4296 characters. It can also store special characters as well. As soon as the data size increases, the structure of the QR Code becomes more complex.</p><br>
          <h2 class="w3-text-teal">Advantages</h2>
          <p>QR codes are beneficial to both customers and business owners and can be used for probably everything. The business owners save money for advertising costs by sharing their website URLs. QR codes also bridge various marketing streams together, QR codes act as the link between the customers and business owner's forms, services and much more. With this strategy, a business owner can generate revenue for the business from the digital platform.</p>
          <h2 class="w3-text-teal">How to create a QR Code?</h2>
          <p>You can check out above, we have developed a tool to generate QR codes. It is a real-time tool for creating QR codes. You can visit here, create QR codes as many as you want to download them totally for free.</p>
          <h2 class="w3-text-teal">Contact us!</h2>
          <p>If you are finding it difficult to create a QR code then do not hesitate to contact us. We would be glad to solve your problems.</p>
        </div>
        <div class="w3-third w3-container">
          <p class="w3-border w3-padding-large w3-padding-32 w3-center">AD</p>
          <p class="w3-border w3-padding-large w3-padding-64 w3-center">AD</p>
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
  title: 'QR code generator – Create codes for free from this Generator',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Generator QR codes easily with our free online tool – QR Code Generator. Visit the website and generate the QR code in the most pleasant way.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/qr-code-generator/'}
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
            text_val: null,
            title: "QR code generator",
            message: ''
    }
  },
  methods: {
   reset() {
     this.message = '',
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
