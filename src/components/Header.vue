<template>
  <header class="jumbotrone-section">
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
        {
          text: "DONATE",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.menu a {
  color: white;
}
</style>
