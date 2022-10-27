<template>
  <div style="display:flex; align-items: center; justify-content: space-between;">
    <div style="display: flex; font-size: .75rem; color: red;">
      <div style="margin: 1em 1em 1em 0em" v-for="list in list_top" :key="list">
        <div>{{list}}</div>
      </div>
    </div>
    <div style="display:flex; font-size: .75rem; color: red;">
      <div>English</div>
      <div style="color:black; margin-left: 1em;">Bahasa Indonesia</div>
    </div>
  </div>
  <div class="menubar__list">
    <div style="display:flex; align-items:center">
      <div style="display:grid; justify-items:center">
        <img src="@/assets/logo_indosat.png" height="70" />
        <span style="color:red; font-weight: bold; font-size: .75rem;">ini baru internetan seru</span>
      </div>
      <div style="margin: 0.5em" v-for="list in list_menu" :key="list">
        <div>{{ list }}</div>
      </div>
    </div>
    <input class="search__bar" placeholder="search"/>
  </div>
</template>

<script>
export default {
  name: "MenuBar",
  data() {
    return {
      list_menu: ["Products", "Why IM3 Ooredoo", "Shop", "myIM3", "Buy SIM Card"],
      list_top: ["Personal", "Business", "About Indosat Oredoo", "Investor Relation"],
      laguange: ['English', 'Bahasa Indonesia']
    };
  },
};
</script>

<style>
.menubar__list {
  display: flex;
  background-color: white;
  box-shadow: 2px 2px 4px #a3a3a3;
  padding: 0.5em 5em;
  border-radius: 1em;
  align-items:center;
  justify-content: space-between
}
.search__bar {
  height: 1.5em;
  border-radius: 1em;
  padding: 0.25em 0.75em;
  border: none;
  box-shadow: 1px 1px 3px #545454;
}
.languange {
  color: red
}
</style>
