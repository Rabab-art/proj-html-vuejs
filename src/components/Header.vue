<template>
  <header class="jumbotrone-section">
    <!-- inserimento della struttura per la navbar -->
    <section class="container">
      <div class="row  p-2 d-flex justify-content-end">
        <div class="col">
          <img src="../assets/avada-charity-sticky-header-logo.png" alt="" />
        </div>
        <div class="col">
          <ul>
            <li
              v-for="item in items"
              :key="item.id"
              class="menu d-inline-block p-3 "
            >
              <a href="">{{ item.text }}</a>
             
            </li>
             <input class="orange" type="submit" value="DONATE">
          </ul>
        </div>
      </div>
      <HeaderJumbo /> 
    </section>
  </header>
</template>

<script>
import HeaderJumbo from "@/components/HeaderJumbo.vue";
export default {
  name: "Header",
  components: {
    HeaderJumbo,
  },
// creazione di un array per il menu della navbar

  data() {
    return {
      items: [
        {
          text: "HOME",
        },
        {
          text: "MISSION",
        },
        {
          text: "CAUSES",
        },
        {
          text: "JOURNAL",
        },
       
      ],
    };
  },
};
</script>

<style lang="scss" scoped>

</style>
