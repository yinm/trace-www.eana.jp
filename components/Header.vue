<template>
  <header class="transparent">
    <nav
      :class="{scroll: isScrolled}"
      class="pc-menu">
      <a
        class="logo-row"
        href="#">
        <div class="logo"/>
      </a>

      <ul class="menu">
        <li class="current">
          <a
            href="#"
            class="font-ss">INDEX</a>
        </li>
        <li>
          <a
            href="#"
            class="font-ss">WORKS</a>
        </li>
        <li>
          <a
            href="#"
            class="font-ss">PUBLICATIONS</a>
        </li>
        <li>
          <a
            href="#"
            class="font-ss">PROFILE</a>
        </li>
        <li>
          <a
            href="#"
            class="font-ss">ACCESS & CONTACT</a>
        </li>
      </ul>

      <ul class="list-sns">
        <li class="icon-f">
          <a href="#">F</a>
        </li>
        <li class="icon-in">
          <a href="#">I</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
  export default {
    data() {
      return {
        isScrolled: false
      }
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll)
    },
    methods: {
      handleScroll() {
        this.isScrolled = window.scrollY > 300
      }
    }
  }
</script>

<style scoped>

header nav.pc-menu {
  background: #fff;
}
  header.transparent nav.pc-menu {
    background-color: transparent;
  }

  header nav.pc-menu {
    position: fixed;
    z-index: 200;
    width: 100%;
    height: 60px;
    box-sizing: border-box;
    padding: 0 1.3% 0 2.34%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  header nav.pc-menu a.logo-row .logo {
    width: 90px;
    height: 33px;
    background: #222;
  }

  header nav.pc-menu a.logo-row {
    opacity: 0;
    height: 33px;
  }

  header nav.pc-menu ul li {
    display: inline;
  }

  header nav.pc-menu ul.menu {
    min-width: 500px;
    margin-right: 3%;
  }

  header nav.pc-menu ul.list-sns li.icon-f {
    margin-right: 4px;
  }

  header nav.pc-menu ul.menu li {
    margin-right: 27px;
  }

  header nav.pc-menu ul.menu li:last-of-type {
    margin-right: 0;
  }

  header nav.pc-menu ul.menu li.current a {
    border-bottom: 2px solid #fff;
    padding-bottom: 6px;
  }

  header nav.pc-menu ul.menu li a {
    text-decoration: none;
    color: #fff;
    letter-spacing: 0.03em;
  }

  header nav.pc-menu ul.list-sns li a {
    text-decoration: none;
    color: #fff;
    letter-spacing: 0.03em;
  }

  header.transparent nav.pc-menu {
    transition: background 0.5s ease;
    background: rgba(255, 255, 255, 0);
  }

  header.transparent nav.pc-menu.scroll {
    background: rgba(255, 255, 255, 1);
  }

  header nav.pc-menu.scroll a.logo-row {
    opacity: 1;
  }

  header nav.pc-menu.scroll ul.menu li a {
    color: #222;
  }

  header nav.pc-menu.scroll ul.list-sns li a {
    color: #222;
  }

  header nav.pc-menu.scroll ul.menu li.current a {
    border-bottom-color: #222;
    padding-bottom: 4px;
  }

</style>
