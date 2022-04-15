<template>
  <div class="top-section">
    <div class="top-container">
      <div class="market-input">
        <div class="text-con">
          <p class="pass">In the past 24hrs</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PriceTop",
};
</script>

<style scoped>
.top-section {
  padding: 25px 0;
}
.top-container {
  width: 85%;
  margin: 0 auto;
}
.text-con {
  margin-bottom: 15px;
  /* font-size: 12px; */
}
.pass {
  font-weight: 600;
  color: rgb(14, 73, 75);
}
.market {
  font-size: 24px;
  font-weight: 600;
}
.market-input {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 20px;
}
.down {
  color: rgb(211, 16, 16);
}
.card-container {
  display: none;
}
.card-mobi {
  display: flex;
  flex-direction: column;
  border: 1px solid gainsboro;
  padding: 15px 10px 10px;
  border-radius: 8px;
}
.mobi-flex {
  display: flex;
  align-items: center;
  margin-bottom: 25px;
  margin-left: 10px;
}
.mobi-flex img {
  width: 15%;
}
.see {
  text-align: center;
  font-weight: 600;
}
.mobi-in {
  margin-left: 30px;
}
@media only screen and (min-width: 992px) {
  .top-section {
    padding: 25px 0;
  }
  .top-container {
    width: 85%;
    margin: 0 auto;
  }

  .text-con {
    margin-bottom: 15px;
  }
  .pass {
    font-weight: 600;
    color: rgb(14, 73, 75);
  }
  .market {
    font-size: 24px;
    font-weight: 600;
  }
  .market-input {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 0;
  }
  .mobi-container {
    display: none;
  }
  input {
    width: 600px;
    height: 40px;
    font-family: inherit;
    padding: 15px;
    font-size: 16px;
  }
  .down {
    color: rgb(211, 16, 16);
  }
  .card-container {
    display: flex;
    height: 200px;
  }
  .card {
    width: 25%;
    margin: 8px;
    border: 1px solid gainsboro;
    border-radius: 10px;
    padding: 15px;
  }
  .card img {
    width: 20%;
    margin-top: 15px;
  }
  .card-name {
    margin-top: 10px;
  }
  .card-info {
    margin-top: 10px;
  }
}
</style>
