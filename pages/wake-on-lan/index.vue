<template lang="html">
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Wake-On-Lan(WOL): Everything you need to know</h1>
          <article>
            Wake-on-LAN also known as WOL is a protocol to wake up the computer over the LAN by a network message which is called “Magic Packet”. This magic packet is sent to the MAC address of the system which we want to turn on over the network layer. It is also possible to wake the system from a different network, for that you need gateway services.<br><br>
            <b>How does Wake-on-LAN Work?</b><br><br>
            The computers configured with Wake-on-LAN configuration eventually wait for the magic packet to deliver which includes the MAC address of the system and a particular message for that system. That message wakes up a sleeping computer system over the network. But, here the only condition is that the sender and the receiver must in the same network and if you want to wake the system which is located in a different network then you need to configure it using subnet directed broadcasts or WOL gateway service.<br><br>
            <b>About Magic Packet in Wake-On-LAN</b><br><br>
            The magic packet is a frame that contains 6 bytes of Hexadecimal number. The magic packet is not parsed by the full protocol stack it can be sent as any network layer protocol but still it has some limitations. Once you send a magic packet, you will not get acknowledgment from the other system once it receives the frame. The MAC address of the destination system is required otherwise you won’t be able to perform Wake-on-LAN configuration.<br><br>
            <b>MAC Address:</b><br><br>
            MAC address can be defined as the unique identity number of any system just like your username of twitter. Every system has one mac address which is unique and not any other system has that MAC address. To find out your system’s mac address just type ipconfig /all in the windows command-line interface and you will receive address in response. Not only computer systems but all the switches, routers, play stations, X-boxes have a unique mac address.<br><br>
            <b>Node.js code for WOL</b><br><br>
            To build a computer program of WOL, you need to install a third-party package for node.js. For Linux add the following command in the terminal,<br><br>
            <code style="background-color: lightgreen;">$ [sudo] npm install [-g] wol --save</code><br><br>
            If you are a windows user then add the following command in the windows command-line interface, make sure you are in the correct directory,<br><br>
            <code style="background-color: lightgreen;">npm i wol –save</code><br><br>
            To build your own program, you need the mac address of the destination system where you want to send the magic packet, to get the mac just type the following command in the windows terminal,<br><br>
            <code style="background-color: lightgreen;">Ipconfig /all</code><br><br>
            By typing this command, you will get MAC of the system,
            <b>code</b><br><br>
            <div style="background-color: lightgreen;">
            <code>const wol = require(’wol’);</code><br>
            <code>wol.wake(’20:AE:44:DE:45:CD’, err, res =>{</code><br>
            <code>console.log(res);</code><br>
            <code>})</code>
          </div><br><br>
          <h2><b>What's Next?</b></h2><br>
          We are currently developing our Wake-on-LAN tool from which you will be able to switch on the sleeping computer system from either a different system or your smart phone. But, our tool will only work for the systems which are connected to the same network. Not only for computers, we are also developing a tool for waking up the play station 4 and X-box from the same LAN. For more details about our tool, do check back soon in a few days.
          </article>
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
  title: 'Wake-on-lan detailed information. Code, difinition and magic packets',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'wake-on-lan widely popular among the techies is the protocol to wake a computer from over the network layer. Some call it wol. Get the detailed information about wake-on-lan here.' },
      { hid: 'robots', name: 'robots', content: 'noindex,nofollow' }
  ],
  link: [
 {rel: 'canonical', href: 'https://binarytotext.net/wake-on-lan/'}
]
}
},
  components:{
    'footer-app': footer
  },
}
</script>

<style scoped>
</style>
