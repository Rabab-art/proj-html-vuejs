<template>
  <header class="">
    <div class="row container-sm text-center">
      <div class="col">
        <img src="../assets/avada-charity-sticky-header-logo.png" alt="" />
      </div>
      <div class="col">
        <ul >
          <li v-for="item in items" :key="item.id" class="d-inline-block p-3 ">
              <a href="">{{item.text}}</a>
          </li>
        </ul>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
data(){
    return{
  items:[
    {
        text:'home',
    },
    {
        text:'mission',
    },
    {
        text:'causes',
    },
    {
        text:'journal',
    },
    {
        text:'donate',
    },
   ]
    };
},
};
</script>

<style lang="scss" scoped></style>
