<template lang="html">
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">LAN(Local Area Network) - Concept, Definition, Commands</h1>
          <article>
            This is the era of smartphones, the world is changing and so is the world of networking. Starting from the Hubs in the 1990s to the routers, Layer-2, Layer-3 switches improvising the concept of Local Area Network(LAN).
          <br><br>
          <b>What is LAN(Local Area Network)?</b><br><br>
            LAN is Local Area Network, where all the systems like computers, printers, master computers which have a MAC address are connected via Lan cables and switches. A LAN is limited to the specific areas such as schools, colleges, banks or private offices. The systems can only get access to the transfers only with the systems which are connected on the LAN. Systems can communicate with each other even in the absence of the internet layer.
          <br><br>
          <b>Useful LAN Commands:</b>
          <br><br>
            <b>Ping</b><br>
            By typing the ping in the command line interface, you will be able to see the bunch of commands options that can be helpful. Some of them are -t, -a, -n, -f and so on.
          <br>
          <b>Ipconfig</b><br>
          With Ipconfig command, you will be able to see the windows IP configuration on your system which is connected to the internet or it is in the LAN. If you are connected with the internet on the WIFI then you will get “Wireless LAN Adapter”. Under this section, you will find IPV6 address, Subnet mast of your system, default gateway, IPV4 LAN address.<br><br>
          <b>Ping – 192.168.43.10</b><br>
          With this command, you can check whether your system is connected with the network or not. By typing Ipconfig, you will find out the LAN address of your system. Once you find the LAN address, you will be able to ping on that address and check the local area connection.<br><br>
          <b>Ping – 192.168.8.10 -t</b><br>
          This is the same command as above, but with this command, the loop will keep on running until you stop it manually. For example, if you are testing a computer system which is connected in the LAN, you can use this command to find out whether the system is getting signals from the server or not. This is one of the most popular and commonly used command in the networking industry. If you are in the same industry, then you will use this command several times. Not only in the computer system checking but, configuring the switches or the routers.<br><br>
          <b>NetStat</b><br>
          Netstat shows the network connection for the TCP, the network interfaces, routing tables, and network statistics and much more in detail.<br><br>
          <b>ARP</b><br>
          ARP stands for address resolution protocol which simply helps the users to find out the physical address, internet address and shows the types of address (dynamic or static). Normally, dynamic addresses keep on changing, for example, if you connect with the WIfi then your IP address can be 192.168.43.14, once you disconnect and then connect with the same Wifi then the IP might be changed. With ARP -a command you will be able to find out all this information about a particular system and the network connectivity.<br><br>
          <b>NSLookup</b><br>
          The nslookup commands give back the name of the IP address of the server’s default DNS record.<br><br>
          <b>Route</b><br>
          In the network topology, all the files are transferred in the form of packets. To transfer these file packets from one subnet to another, networks use routing tables. With route command, you can view your devices’ routing table. Not only that, but you can also edit the routing table.<br>
          This command is useful if your network is receiving a lot of traffic from the other systems. You can update routing table to by adding a new route or updating the existing route or delete a whole route.<br><br>
          <b>Pathping</b><br>
          Pathping – 192.168.43.14 traces route to the given IP address (192.168.43.14) over a maximum of 30 hops. With this command, you will get the hostname and along with that IP address of your system.<br><br>
          <b>Addresses in LAN:</b><br>
          In most cases, the structure of LAN addresses is 192.168.x.x. Here, 192.168 shows you are at the local area, the third digit shows the network number. For example, if you are at the 192.168.6, it means that your network number is 14. The last digit in the address is the port number of the network. For example, if you are at 19.168.6.43 then it means the network number is 6 and the port number is 43.<br><br>
          <b>Important LAN Components:</b><br><br>
          <b>Switches</b><br>
          If you are familiar with the LAN architecture, then you definitely know about switches. Switches are either 24 Port or 48 port. After hubs, switches took over the networking market and currently there are two types of switches available in the market. The first is Layer 2 switches and another Layer 3 switches. Small to medium organizations use layer 2 switches while big organizations use layer 3 switches. The layer 2 switches can only communicate and share data among the same network while layer 3 switches can communicate in a different network.<br><br>
          <b>Routers</b><br>
          A Router is a smart device which is widely used to send data packets from one system to the another. In some cases, they are used to send the packets in the same network while in other cases they are used to send packets to the different network.<br><br>
          <b>Ethernet Cables</b><br>
          In simple words, Ethernet cables connect devices within a Local area network(LAN) such as PCs, printers, routers, switches, etc. There are various types of Ethernet cables specially built to perform different kinds of tasks for a network system. There are different types of Ethernet cables and that include category 5, category 6, and now some networking companies use category 7 cables for the faster and better packet transmission. Most technicians refer these cables like cat5, cat6 and cat 7 cables.
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
  title: 'What is local area network? Find out definition, important commands to become networking expert',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: [
      { hid: 'description', name: 'description', content: 'Local area network is a network which connects various systems which are in the same network. Switches, routers, etnernet cables are the important components.' },
      { hid: 'robots', name: 'robots', content: 'noindex,nofollow' }
  ],
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/lan-local-area-network/'}
  ]
  }
  },
  components:{
    'footer-app': footer
  },
}
</script>

<style lang="css">
</style>
