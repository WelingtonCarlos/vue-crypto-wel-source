<template>
  <footer>
    <div class="footer-container">
      <div class="center">
        <div>
          <router-link to="/">
            <img src="../assets/logo.svg" alt="" />
          </router-link>
        </div>
        <p class="base">© 2022 Coin-Wel</p>
        <p class="socials">
          <a href="https://www.linkedin.com/in/welington-carlos-b3825a153/"
            >Linkedn</a
          >
          • <a href="https://github.com/WelingtonCarlos">Github</a> •
          <a href="https://wcfilho98@hotmail.com">Outlook</a>
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style scoped>
a {
  text-decoration: none;
  color: rgb(14, 73, 75);
}

a:hover {
  text-decoration: underline;
}

footer {
  padding-top: 100px;
  padding-bottom: 100px;
}
.footer-container {
  border-top: 1px solid rgb(14, 73, 75);
  display: flex;
  width: 85%;
  margin: 0 auto;
  flex-direction: column;
}
.center {
  margin: auto;
  margin-top: 16px;
  width: max-content;
  font-size: 18px;
  color: rgb(14, 73, 75);
}
img {
  width: 100%;
}
.base {
  margin-top: 15px;
}
.socials {
  margin-top: 5px;
}

@media only screen and (min-width: 992px) {
  footer {
    padding-top: 100px;
    padding-bottom: 100px;
  }
  .footer-container {
    flex-direction: row;
    width: 85%;
    margin: 0 auto;
  }
  select {
    font-family: inherit;
    width: 250px;
    height: 30px;
    font-size: 16px;
    font-weight: 500;
    margin-top: 20px;
  }
  img {
    width: 100%;
  }
}
</style>
