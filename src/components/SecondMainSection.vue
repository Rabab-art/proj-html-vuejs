<template>
  <main>
    <section class="second-main-section jumbotrone-section text-center">
        <!-- seconda sezione del Main ripartita per contenere diversi elementi -->
      <div class=" row p-5 text-center ">
        <div class="col p-5 align-item-end h-100">
          <h2 class="p-3">OUR VALUES</h2>
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
        <div v-for="value in values" :key="value.id" class="col mt-5">
          {{ value.text }} <br>
          <input class="button-learn p-1 orange" type="submit" value="LEARN MORE"/>
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
          text:
            "Litterae non intrant sine sanguine, litterarum radices amarae, fructus dulces.",
        },
        {
          text:
            "Litterae non intrant sine sanguine, litterarum radices amarae, fructus dulces.",
        },
        {
          text:
            "Litterae non intrant sine sanguine, litterarum radices amarae, fructus dulces.",
        },
        {
          text:
            "Litterae non intrant sine sanguine, litterarum radices amarae, fructus dulces.",
        },
      ],
    };
  },
 
};
</script>

<style lang="scss" scoped>
</style>
