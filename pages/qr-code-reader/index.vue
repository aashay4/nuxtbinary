<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">QR Code Reader</h1>
          <p>Finding a tool to read a QR code? You are in the right place, our tool helps you to read different QR codes very easily. With our QR code reader, you can upload a file and read what is there in the QR code or use the camera to scan QR codes. Our tool is free and you can read as many codes as you want.</p>
          </div>
        </div>
      <div class="w3-row" style="text-align: justify;">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">What is the process of our QR Code Reader?</h1>
            <p>There are two ways you can use our tool for the QR code reading. The first way is by uploading the file which you already have downloaded. You just need to upload it, our tool will scan the QR code automatically and show the results in the box. The second way is by scanning the physical QR with the help of your camera. This is a very popular way of QR code scanning. To use this feature, you need to permit our app to access the cameras on your device.</p><br>
            <b>What you can scan?</b>
            <p>Whenever you buy a new headphone, charger or any other electronic device, there is already a QR code attached with it. You can scan that QR code with the help of our tool and get to know about the precise date when it is expiring? Apart from that, you can also save address, emails, and websites as this code and whenever you need them you can use this tool and get the desired information.</p>
            <b>Benefits?</b>
            <p>If you want to keep some texts of data secretly then you can use Qr codes. By generating codes, no one would be able to read what is inside of that code and your data will remain safe. Many big organizations are using QR codes while sending sensitive information over the internet layer. You can also save your important document with these codes. While scanning, you can use our tool as it is free, as you can scan as many codes as you want.</p>
            <p>If you have any suggestion for our tool or finding it difficult to use then do contact us. We would appreciate your feedback.</p>
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
  title: 'QR Code Reader – Scan your QR Codes from this Online Scanner',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Best online QR code reader. Visit our website and scan QR codes very easily.' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/qr-code-reader/'}
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
            result: '',
            text_val: null,
            title: "QR code generator",
            error: "",
            styleObject: {
            color: 'green',
            fontSize: '25px'
          }
}
},
  methods: {
    async onInit (promise) {
      try {
        await promise
      } catch (error) {
        if (error.name === 'NotAllowedError') {
          this.error = "ERROR: you need to grant camera access permisson"
        } else if (error.name === 'NotFoundError') {
          this.error = "ERROR: no camera on this device"
        } else if (error.name === 'NotSupportedError') {
          this.error = "ERROR: secure context required (HTTPS, localhost)"
        } else if (error.name === 'NotReadableError') {
          this.error = "ERROR: is the camera already in use?"
        } else if (error.name === 'OverconstrainedError') {
          this.error = "ERROR: installed cameras are not suitable"
        } else if (error.name === 'StreamApiNotSupportedError') {
          this.error = "ERROR: API is not supported in this browser"
        }
      }
    },
    onDecode (result) {
      this.result = result
    },
   reset() {
     this.message = '',
     this.text_value= null
   }
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
</style>
