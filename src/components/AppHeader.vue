<template>
  <div class="con">
    <header>
      <nav id="nav" @mouseleave="hideLinks">
        <router-link class="link link-logo" to="/">
          <span>COIN-WEL</span>
        </router-link>
        <ul class="link-wrapper">
          <li>
            <router-link to="/prices"
              ><button class="nav-btn" to="/prices">Prices</button></router-link
            >
          </li>
        </ul>
        <i
          @click="toggleShow"
          v-if="show === true"
          class="fas fa-times fa-lg"
        ></i>
      </nav>
    </header>
  </div>
</template>

<script>
export default {
  methods: {
    toggleShow() {
      this.show = !this.show;
    },
  },
};
</script>

<style scoped>
.con {
  position: -webkit-sticky;
  position: sticky;
  top: 0;
  z-index: 1;
  width: 100%;
  margin-bottom: 64px;
}

header {
  height: 60px;
  background-color: white;
  border-bottom: 1px solid rgb(236, 239, 241);
}

span {
  color: rgb(14, 73, 75);
  font-size: 32px;
}

#nav {
  display: flex;
  width: 90%;
  height: 60px;
  margin: 0 auto;
  align-items: center;
}

#nav a {
  text-decoration: none;
  color: rgb(5, 15, 25);
  font-weight: 900;
}

.link-logo {
  flex-grow: 1;
}

.link {
  display: block;
  width: 100%;
}

img {
  width: 200%;
}

.fa-bars,
.fa-times {
  margin-left: 20px;
  color: grey;
  cursor: pointer;
}

.link-wrapper li {
  list-style-type: none;
  font-size: 15px;
  height: 56px;
  display: flex;
  align-items: center;
  border-bottom: 4px solid white;
}

li:hover {
  border-bottom: 4px solid rgb(14, 73, 75);
  width: max-content;
}

.nav-btn {
  display: block;
  font-family: inherit;
  border: 1px solid rgb(14, 73, 75);
  background-color: rgb(14, 73, 75);
  line-height: 14px;
  width: 120px;
  height: 40px;
  border-radius: 4px;
  color: white;
  font-size: 18px;
  font-weight: 500;
}

.nav-btn:hover {
  cursor: pointer;
}

.btn-container {
  display: flex;
  flex-direction: column;
}

.learn-section,
.indi-section {
  display: none;
}

@media only screen and (min-width: 992px) {
  .con {
    position: -webkit-sticky;
    position: sticky;
    top: 0;
    z-index: 1;
    width: 100%;
  }
  header {
    height: 60px;
    background-color: white;
    border-bottom: 1px solid rgb(236, 239, 241);
  }

  .fa-bars {
    display: none;
  }
  #nav {
    display: flex;
    width: 80%;
    height: 60px;
    margin: 0 auto;
    align-items: center;
  }

  #nav a {
    text-decoration: none;
    color: rgb(5, 15, 25);
    font-weight: 900;
  }

  .link {
    width: 20%;
  }

  .link-wrapper {
    flex-grow: 0.3;
    display: flex;
  }

  .link-wrapper li {
    list-style-type: none;
    font-size: 22px;
    height: 56px;
    display: flex;
    align-items: center;
    border-bottom: 4px solid white;
    margin: auto;
  }

  li:hover {
    border-bottom: 4px solid rgb(14, 73, 75);
  }

  button {
    display: block;
    font-family: inherit;
    border: 1px solid rgb(14, 73, 75);
    background-color: rgb(14, 73, 75);
    font-weight: 900;
    line-height: 14px;
    width: 120px;
    height: 40px;
    border-radius: 4px;
    color: white;
    right: 0;
  }
}
</style>
