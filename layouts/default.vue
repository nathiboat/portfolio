<template>
  <div class="container-fluid">
    <div class="row d-flex">
      <div id="side" class="dark multiple-desktop col-sm-3 col-md-2 d-none d-sm-block bg-light sidebar">
        <img src="/img/me.png" class="profile img-fluid">
        <ul class="menu">
          <li v-for="item in sidebar"><nuxt-link :to="item.index">{{item.name}}</nuxt-link></li>
        </ul>
        <footer>
          <ul class="icons">
            <li v-for="item in footer"><a :href="item.link" target="_blank" class="fa " :class="item.icon"><span class="label">Twitter</span></a></li>
          </ul>
        </footer>
      </div>
      <main id="main" class="col-sm-9 ml-sm-auto col-md-10 pt-3">
        <nuxt/>
      </main>
      <input type="button">
    </div>
  </div>
</template>

<script>
  export default{
    data () {
      return {
        sidebar: [
          {name: 'About', index: '/about'},
          {name: 'Side Project', index: '/about'},
          {name: 'Contact', index: '/contact'}
        ],
        footer: [
          {link: 'https://twitter.com/NathiBoat', icon: 'fa-twitter'},
          {link: 'https://www.facebook.com/nathi.taengnim', icon: 'fa-facebook'},
          {link: 'http://instagram.com/nathiboat/', icon: 'fa-instagram'},
          {link: 'https://github.com/nathiboat', icon: 'fa-github'},
          {link: 'http://codepen.io/nathiboat/', icon: 'fa-codepen'}
        ]
      }
    }
  }
</script>
<style>
  body{
    background: #d2dbd1
  }
  #side {
    position: fixed;
    z-index: 1000;
    padding: 20px;
    overflow-x: hidden;
    overflow-y: auto;
    border-right: 1px solid #eee;
    position: fixed;
    height: 100%;
    padding: 15px;
  }
  .dark.multiple-desktop {
    background-image: url(/img/dark-bg.jpg);
  }
  .light.multiple-desktop {
    background-image: url(/img/light-bg.jpg);
  }
  .multiple-desktop {
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    background-repeat: no-repeat;
  }

</style>

