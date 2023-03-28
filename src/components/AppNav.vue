<script>
export default {
  name: "AppNav",
  data() {
    return {
      links: [
        {
          text: 'characters',
        },
        {
          text: 'comics',
        },
        {
          text: 'movies',
        },
        {
          text: 'tv',
        },
        {
          text: 'games',
        },
      ],

      activeIndex: 2,

    }
  },

  methods: {
    changeIndex(newIndex) {
      this.activeIndex = newIndex;
    }
  }
}
</script>

<template>
  <nav>
    <div class="container">
      <div id="logo">
        <img src="/img/dc-logo.png" alt="">
      </div>

      <ul class="links">
        <li v-for="(link, index) in links" class="link" :class="activeIndex == index ? 'active' : ''" @click="changeIndex(index)">
          <a href="#">{{link.text}}</a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
@use "../scss/variables" as *;


  nav {

    background-color: white;

    width: 100%;
    height: 80px;

    .container {
      display: flex;
      justify-content: space-between;
      align-items: center;

      width: 100%;
      height: 100%;
    }

    #logo {
      height: 100%;

      padding: 10px;


      img {
        height: 100%;
      }

    }


    .links {
      display: flex;
      flex-flow: row;
      justify-content: flex-end;
      gap: 20px;

      height: 100%;


      text-transform: uppercase;

      color: #333;


      .link {
        position: relative;
        display: inline-block;
        display: flex;
        align-items: center;
        height: 100%;

        font-weight: bold;
        


        a {
          color: inherit;
          text-decoration: none;
        }

        &.active {
          color: $primary;
          
          // border-bottom: 3px solid $primary;

          &::before {
            content: '';

            position: absolute;
            bottom: 0;

            width: 100%;
            height: 5px;



            background-color: $primary;
          }
        }


        &:hover {
          color: $primary;
        }
      }
    }
    

  }
</style>