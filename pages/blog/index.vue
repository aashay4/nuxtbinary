<template>
  <div>
    <div class="w3-main" style="margin-left:250px">
      <div class="w3-row w3-padding-64">
        <div class="w3-twothird w3-container">
          <h1 class="w3-text-teal">Blog</h1>
          <input type="text" v-model="search" style="width: 100%;" placeholder="Custom Search" /><br>
        <section>
          <postpreview class="single-blog borderli" v-for="post in filteredPosts"
          :key="post.id"
          :title="post.title"
          :excert="post.previewText"
          :id="post.id" />
        </section>
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
import postpreview from '~/components/postpreview.vue';
import footer from '~/components/footer.vue';

export default {

  meta: {
  // sets document title
  title: 'Blog | Get the latest new and know whats hapenning in tech world',
  // optional; sets final title as "Index Page - My Website", useful for multiple level meta
  // meta tags
  meta: {
    description: { name: 'description', content: 'Read our blog posts find our what is happening in the technology world. Subcribe today for the news latter.' },
    equiv: { 'http-equiv': 'Content-Type', content: 'text/html; charset=UTF-8' }
  },
  link: [
  {rel: 'canonical', href: 'https://binarytotext.net/blog/'}
  ]
  },
  components:{
    'postpreview': postpreview,
    'footer-app': footer
  },
  data () {
    return {
    posts: [
      {
      title: 'How to Write 2 in binary',
      id: '/2-in-binary/'
    },
    {
      title: 'Write number 6 in binary',
      id: '/write-6-in-binary/'
    },
    {
      title: 'how to Write Number 10 in binary',
      id: '/how-to-write-10-in-binary/'
    },
    {
      title: 'Number 22 in binary',
      id: '/22inbinary/'
    },
    {
      title: '3 in binary',
      id: '/3-in-binary/'
    },
    {
      title: '8, 1, 16, 12, 100, 5, 7, 128, 42, 15, 256, 64, 11, 9, 20, 14, 32, 25 in binary numbers',
      id: '/binary-numbers/'
    },
      {
      title: 'LAN(Local Area Network) - Concept, Definition, Commands',
      id: '/lan-local-area-network/'
    },
      {
      title: 'Wake-On-LAN(WOL): Everything You Need to Know',
      id: '/wake-on-lan/'
    }
],
search: ''
}
},
  computed: {
    filteredPosts: function(){
      return this.posts.filter((post) => {
        return post.title.match(this.search);
      });
    }
  }
  }
</script>

<style scoped>

#posts {
  padding-top: 2rem;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.single-blog {
  box-sizing: border-box;
  border-bottom: 1px solid silver;
  padding-top: 10px;
}

.borderli {

}

@media (min-width: 35rem) {
  #posts {
    flex-direction: row;
  }
}
</style>
