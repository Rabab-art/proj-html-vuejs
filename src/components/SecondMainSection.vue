<template>
  <main>
    <section class="second-main-section jumbotrone-section text-center">
      <!-- seconda sezione del Main ripartita per contenere diversi elementi -->
      <div class=" row p-5 text-center ">
        <div class="col p-5 align-item-end h-100">
          <h2 class="p-2">OUR VALUES</h2>
          <div class="b-line"></div>
          <h5 class="p-3">Think Big.Act Bigger.</h5>
        </div>
      </div>
      <div class="row">
        <div class="col"></div>
        <div class="col"></div>
        <div class="col"></div>
        <div class="col"></div>
      </div>
      <div class="row p-3 values">
        <!-- creazione di v-for che cicla i testi delle colonne    -->

        <div v-for="value in values" :key="value.id" class="col mt-3">
          <div class="icon "><font-awesome-icon :icon="['fas', value.icon ]"/></div>
        <div class="title"> {{ value.title }}</div>
          <p class="p-3">{{ value.text }}</p>
          
          <input
            class="button-learn p-1 orange"
            type="submit"
            value="LEARN MORE"
          />
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: "SecondMainSection",

  data() {
    return {
      values: [
        {
          icon:'tint',
          title:'Clean water',
          text:
            "Litterae non intrant sine sanguine, litterarum radices amarae, fructus dulces.",
        },
        {
          icon:'stethoscope',
          title:'Vaccinations',
          text:
            "Litterae non intrant sine sanguine, litterarum radices amarae, fructus dulces.",
        },
        {
          icon:'graduation-cap',
          title:'Education',
          text:
            "Litterae non intrant sine sanguine, litterarum radices amarae, fructus dulces.",
        },
        {
          icon:'seedling',
          title:'Framing',
          text:
            "Litterae non intrant sine sanguine, litterarum radices amarae, fructus dulces.",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.icon{
font-size: 70px;
color: rgb(251, 181, 50);
}

.title{
  font-size: 25px;
}
</style>
