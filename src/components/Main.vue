<template>
  <main>
    <section class="first-sect-main  ">
        <!-- PRIMA SEZIONE DEL MAIN CREAZIONE DI DUE COLONNE DI MISURA DIVERSA  -->
      <div class="row no-gutters  justify-content-center m-auto">
        <div class="col-md-8 p-5 ml-1">
          <h2 class="mb-3">EVERY MOMENTS COUNTS</h2>
           <div class="left-b-line  "></div>
        
          

          <p>
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nesciunt
            ad incidunt quia voluptates in? At cum quae temporibus vero,
            officiis qui odio quasi blanditiis reprehenderit recusandae quidem
            quia perferendis. Reprehenderit?
          </p>
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit.
            Praesentium deserunt in est quam aliquam animi, molestiae veniam a,
            laudantium provident numquam, vel consequuntur fuga tempora corporis
            labore modi laborum vitae!
          </p>
          <p>
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam quo
            provident ducimus ad rerum voluptatibus esse molestiae commodi, hic
            tenetur animi molestias expedita accusamus voluptatem aliquam
            pariatur quisquam eveniet sunt?
          </p> 
          <input class="orange" type="button" name="" id="" value="DONATE">
        </div>

        <!-- v-for per cilare le informazioni della seconda colonna  -->
        <div class="col-md-4 info-charity p-4 text-center">
          <div
           v-for="info in infos"
            :key="info.id"
            class="p-3 mb-3 mt-3 numbers"
            style="color:white"
           
          >{{info.number }}
            <div class="info-charity-text" style="width: 100%" aria-valuenow="100">{{info.item}}</div>
          </div>
        </div>
      </div>
    </section>
    <SecondMainSection/>
    <ThirdMainSection/>
  </main>
</template>

<script>
import SecondMainSection from '@/components/SecondMainSection.vue';
import ThirdMainSection from '@/components/ThirdMainSection.vue';

export default {
  name: "Main",


  data() {
    return {
      infos: [
        {
    
          item: "Volunteers Worldwide",
          number: "2032",
          
        },
        {
          item: "  Active progetcts",
          number: "132",
        },
        {
          item: "  Donated",
          number: "132",
        },
      ],
    };
  },

  components:{
      SecondMainSection,
      ThirdMainSection,
  }
};
</script>

<style lang="scss" scoped>
.first-sect-main {
  max-height: 500px;
}
</style>
