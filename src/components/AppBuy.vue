<script>
export default {
  // aggiunto la proprietà "name" all'export default
  name: 'AppBuy',
  ciao: "",

  data() {
    return {
      buyObjects: [
        {
          title: "Digital Comics",
          img: "buy-comics-digital-comics.png",
        },
        {
          title: "DC Merchandise",
          img: "buy-comics-merchandise.png",
        },
        {
          title: "Subscription",
          img: "buy-comics-subscriptions.png",
        },
        {
          title: "Comic Shop Locator",
          img: "buy-comics-shop-locator.png",
        },
        {
          title: "DC Power Visa",
          img: "buy-dc-power-visa.svg",
        },
      ],
    }

  },
}
</script>

<template>
  <div id="shop-elements-container">

    <a v-for="buyObject in buyObjects" href="#" class="shop-element">

      <img :src="'/img/' + buyObject.img" alt="" class="icon">
      <span class="title"> {{ buyObject.title }} </span>

    </a>

  </div>
</template>

<style lang="scss" scoped>

#shop-elements-container  {
  display: flex;
  flex-flow: row nowrap;
  justify-content: center;
  gap: 70px;

  padding: 50px;
  
  background-color: #0281f8;
  color: white;

  .shop-element {
    display: flex;
    flex-flow: row nowrap;
    align-items: center;
    gap: 1em;

    text-decoration: none;

    .icon {
      height: 3.5em;
    }

    &:last-child .icon { 
      height: 2.8em;
    }

    .title {
      color: white;

      text-transform: uppercase;
    }

  }
}


</style>