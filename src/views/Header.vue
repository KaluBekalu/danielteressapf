<template>
  <header>
    <div class="navigation">
      <h1>Portfoli<span>o</span></h1>
      <nav>
        <ul>
          <li>
            <a href="#about" class="active">About Me</a>
          </li>
          <li>
            <a href="#education">Education</a>
          </li>
          <li>
            <a href="#experiences">Experiences</a>
          </li>
          <li>
            <a href="#certifications">Certifications</a>
          </li>
          <li>
            <a href="#contact">Contact</a>
          </li>
        </ul>
        <i v-if="!menuOpen" @click="toggleMenu" class="menuButton"
          ><MenuIcon fillColor="#FFF"
        /></i>
        <i v-if="menuOpen" @click="toggleMenu" class="menuButton"
          ><CloseIcon fillColor="#FFF"
        /></i>
      </nav>
      <ul v-if="menuOpen" class="mobile-menu">
        <li>
          <a href="#about" class="active" @click="toggleMenu">About Me</a>
        </li>
        <li>
          <a href="#education" @click="toggleMenu">Education</a>
        </li>
        <li>
          <a href="#experiences" @click="toggleMenu">Experiences</a>
        </li>
        <li>
          <a href="#certifications" @click="toggleMenu">Certifications</a>
        </li>
        <li>
          <a href="#contact" @click="toggleMenu">Contact</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<script>
import MenuIcon from "vue-material-design-icons/Menu.vue";
import CloseIcon from "vue-material-design-icons/Close.vue";

export default {
  data() {
    return {
      menuOpen: false,
    };
  },
  components: {
    MenuIcon,
    CloseIcon,
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    },
  },
};
</script>

<style>
header {
  background: #13293e;
  border-bottom: 1px solid white;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 999;
  width: 100%;
}
.navigation {
  position: relative;
  display: flex;
  width: 90%;
  justify-content: space-between;
  height: 5rem;
  align-items: end;
  padding: 0px 3rem 0.9rem 0;
  box-sizing: border-box;
  margin-inline: auto;
  max-width: 1400px;
}

.navigation h1 > span {
  letter-spacing: 0;
}
.navigation h1 {
  color: white;
  letter-spacing: 5px;
  font-weight: 200;
  cursor: pointer;
  margin-bottom: -5px;
}

nav ul {
  display: flex;
  gap: 2rem;
  list-style: none;
}

nav ul li a {
  text-decoration: none;
  color: white;
  font-weight: 200;
  padding-bottom: 5px;
}
nav ul li a::after,
.navigation h1::after {
  content: "";
  width: 0%;
  display: block;
  margin: auto;
  margin-top: 5px;
  transition: 200ms ease;
  border-bottom: 1px solid rgb(255, 0, 0);
}
.navigation h1:hover::after,
nav ul li a:hover::after {
  width: 80%;
  border-bottom: 1px solid rgb(255, 0, 0);
  transition: 400ms ease;
}
.navigation h1:hover,
nav ul li a:hover {
  color: rgb(255, 0, 0);
}

/* nav i:hover {
  transition: 400ms ease;
  color: rgb(255, 104, 104);
} */
nav i {
  font-size: 2rem;
  color: #fff;
  cursor: pointer;
  transition: 400ms ease;
}

.mobile-menu a {
  text-decoration: none;
}
.mobile-menu {
  position: absolute;
  display: none;
  right: 0;
  top: 100%;
  list-style-type: none;
  background: #fff;
  color: #13293e;
  z-index: 20;
  border-bottom: 1px solid #fff;
  box-shadow: rgb(17 17 26 / 10%) 0px 1px 0px, rgb(17 17 26 / 10%) 0px 8px 24px,
    rgb(17 17 26 / 10%) 0px 16px 48px;
}
.mobile-menu li:hover a {
  color: #fff;
  transition: 400ms ease;
}
.mobile-menu li:hover {
  background: #13293e;
  border-bottom: 1px solid #fff;
  transition: 400ms ease;
}
.mobile-menu li:last-child {
  border: none;
}
.mobile-menu li {
  border-bottom: 1px solid #13293e;
  height: 5rem;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 15rem;
  transition: 400ms ease;
}

.menuButton {
  display: none;
}
@media (max-width: 950px) {
  header {
    /* position: relative; */
  }
  .navigation {
    width: 95%;
    padding-right: 0;
  }

  nav ul {
    display: none;
  }
  .mobile-menu {
    display: block;
  }
  .menuButton {
    display: block;
  }
}
</style>
