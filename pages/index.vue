<template>
  <div>
    <div class="navbar">
      <button @click="navigate('https://www.migros.ch/de/offers/home')" class="migros"></button>
      <button @click="navigate('https://www.denner.ch/de/aktionen/list/of/aktionen-aktuelle-woche/')" class="denner"></button>
      <button @click="navigate('https://www.coop.ch/de/aktionen/wochenaktionen/c/m_1011')" class="coop"></button>
      <button @click="navigate('https://www.lidl.ch/c/de-CH/wochenaktion/a10027967?tabCode=Current_Sales_Week')" class="lidl"></button>
      <button @click="navigate('https://www.aldi-suisse.ch/de/aktionen-und-angebote.html')" class="aldi"></button>
      <button @click="navigate('https://www.volg.ch/sortiment/wochenaktionen/')" class="volg"></button>
      <div class="fake"></div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    navigate(link) {
      window.open(link, '_self');
    },
  },
};
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  background-color: #f8f9fa;
  border-bottom: 1px solid #dee2e6;
  z-index: 1000;
}

.navbar button {
  flex: 1;
  border: none;
  background-color: #f8f9fa;
  border-bottom: 1px solid #dee2e6;
  cursor: pointer;
  background-repeat: no-repeat;
  background-position: center;
  background-size: contain;
  border-radius: 0;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  transition: background-color 0.3s, box-shadow 0.3s;
  padding: 0;
  margin: 0;
}

.navbar button:hover {
  background-color: #e2e6ea; 
}

.navbar button:active {
  background-color: #ced4da; 
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1); 
}

.navbar button:last-child {
  border-bottom: none;
}

.fake {
  height: 10%;
  width: 100%;
}

.navbar .migros {
  background-image: url('/migros.png');
}

.navbar .denner {
  background-image: url('/denner.png');
}

.navbar .coop {
  background-image: url('/coop.png');
}

.navbar .lidl {
  background-image: url('/lidl.png');
}

.navbar .aldi {
  background-image: url('/aldi.png');
}

.navbar .volg {
  background-image: url('/volg.png');
}
</style>
