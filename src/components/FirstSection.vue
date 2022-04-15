<template>
  <div>
    <div class="second-section">
      <div class="second-container">
        <h2 class="heading">Listing current prices of major Cryptos.</h2>
        <p class="text">
          Coin-wel is one of the best cryptocurrency listings on the market.
        </p>
      </div>
    </div>

    <div class="first-section">
      <div class="first-container">
        <div class="table">
          <table id="crypto-table">
            <thead class="desk">
              <tr>
                <th>#</th>
                <th>Name</th>
                <th>Price</th>
                <th>Change</th>
              </tr>
            </thead>
            <tbody>
              <tr
                v-for="(crypto, id) in getCrypto.slice(0, 10)"
                :key="crypto.id"
              >
                <td class="id">{{ id + 1 }}</td>
                <td>
                  <div class="tab">
                    <figure>
                      <img :src="crypto.image" alt="" class="crypt-img" />
                    </figure>

                    <p>{{ crypto.name }}</p>
                    <p class="symbol">{{ crypto.symbol.toUpperCase() }}</p>
                  </div>
                </td>
                <td class="price">USD {{ crypto.current_price }}</td>
                <td>
                  <div
                    class="percent"
                    :class="{ red: crypto.price_change_percentage_24h < 0 }"
                  >
                    <p>{{ crypto.price_change_percentage_24h.toFixed(2) }}</p>
                    <i class="fas fa-percent fa-sm"></i>
                  </div>
                </td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { mapActions, mapGetters } from "vuex";

export default {
  name: "FirstSection",
  methods: {
    ...mapActions(["fetchCrypto"]),
  },
  mounted() {
    this.fetchCrypto();
  },
  beforeUpdate() {},
  computed: {
    ...mapGetters(["getCrypto"]),
  },
};
</script>

<style scoped>
.second-section {
  border-bottom: 1px solid gainsboro;
  padding-bottom: 60px;
  margin-bottom: 60px;
}
.second-container {
  width: 85%;
  margin: 0 auto;
}
.heading {
  text-align: center;
  font-size: 40px;
  font-weight: 800;
  color: rgb(12, 62, 64);
}
.text {
  text-align: center;
  color: rgba(12, 62, 64, 1);
  margin-top: 10px;
}

.first-section {
  padding-bottom: 60px;
}
.first-container {
  width: 85%;
  margin: 0 auto;
}
.table {
  display: none;
}
.right-con {
  display: flex;
  align-items: center;
  border: 1px solid gainsboro;
  margin-top: 20px;
}
.crypto {
  display: flex;
  padding: 10px;
}
.crypto h3 {
  margin-left: 20px;
  width: 100px;
  font-size: 22px;
}
span {
  display: none;
}
.fas {
  margin-left: 5px;
}
.percent {
  display: flex;
  align-items: center;
}
.pp {
  color: #098551;
}
.first-section {
  padding-bottom: 80px;
}
.base {
  margin-top: 30px;
  display: flex;
  justify-content: space-between;
}
.right-con {
  display: flex;
  align-items: center;
  border: none;
  margin-top: 0;
}
.crypto {
  display: flex;
  align-items: center;
  padding: 0;
}
.crypto h3 {
  margin-left: 20px;
  width: 220px;
  font-size: 22px;
}
.fas {
  margin-left: 5px;
}
span {
  display: inline;
}
#crypto-table {
  font-family: inherit;
  border-collapse: collapse;
  width: 100%;
  border: 1px solid gainsboro;
  border-radius: 4px;
}
.table {
  display: block;
}

#crypto-table td,
#crypto-table th {
  /* border: 1px solid #ddd; */
  padding: 15px;
}

/* #crypto-table tr:nth-child(odd) {
  background-color: #f2f2f2;
} */

#crypto-table tr:hover {
  background-color: rgb(247, 247, 247);
}

#crypto-table th {
  padding-top: 12px;
  padding-bottom: 12px;
  text-align: left;
  background-color: rgb(14, 73, 75);
  color: white;
}
figure {
  width: 7%;
}
.crypt-img {
  width: 100%;
}
th {
  color: grey;
  font-weight: 200;
  font-size: 16px;
}
tr {
  border-bottom: 1px solid gainsboro;
}
.tab {
  display: flex;
  align-items: center;
}
.tab p {
  margin-left: 10px;
  font-size: 20px;
}
.id {
  color: grey;
}

.symbol {
  color: grey;
  font-weight: 400;
}
.percent {
  display: flex;
  align-items: center;
  color: #098551;
}
.percent p {
  font-size: 18px;
}
.price {
  font-size: 18px;
  font-weight: 400;
}
.trade-btn {
  border: none;
  display: block;
  background-color: #098551;
  color: white;
  font-family: inherit;
  font-weight: 600;
  font-size: 16px;
  border-radius: 4px;
  width: 60px;
  height: 30px;
}
.red {
  color: red;
}
</style>
