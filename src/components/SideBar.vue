<script setup>
import { ref } from 'vue'

const is_expanded = ref(localStorage.getItem("is_expanded") === "true")

const ToggleMenu = () => {
  is_expanded.value = !is_expanded.value

  localStorage.setItem("is_expanded", is_expanded.value)
}
</script>

<template>

  <aside :class="`${is_expanded && 'is-expanded'}`">
    <!-- <router-link to="/">
    <div class="home">
      <img src="../assets/home.png" alt="'home">
    </div>
    </router-link> -->

    <div class="menu-toggle-wrap">
      <button class="menu-toggle" @click="ToggleMenu">
        <img src="../assets/key.png" alt="key" class="key">
      </button>
    </div>

    <h3>Menu</h3> 
    <div class="menu">

      <router-link class="button" to="/">
       <div class="home">
          <img src="../assets/home.png" alt="'home">
       </div>
       <span class="text">Home</span>
    </router-link>

      <router-link class="button" to="/products">
        <div class="products">
          <img src="../assets/Products.png" alt="products" class="products">
        </div>
     <span class="text">Products</span> 
      </router-link>
    </div>

    <div class="flex"></div>

     <div class="menu">

      <router-link class="button" to="/settings">
       <div class="setting">
          <img src="../assets/setting.png" alt="settings">
       </div>
       <span class="text">Settings</span>
      </router-link>
    </div>
  


  </aside>
</template>

<style lang="scss" scoped>
aside {
  display: flex;
  flex-direction: column;
  width: calc(2rem + 32px);
  min-height: 100vh;
  overflow: hidden;
  padding: 1rem;

  background-color: var(--dark);
  color: var(--light);

  transition: 0.2s ease-out;


    @media (max-width: 768px) {
     min-height: 100%;
     
  }
  .flex {
    flex: 1 1 0;

  }
  .home {
    // margin-bottom: 1rem;
    img {
      width: 2rem;
      color: white;
      // background: rgb(190, 175, 175);
    }
  }
  .products {
    // margin-bottom: 1rem;
    img {
      width: 2rem;
      color: white;
      // background: rgb(190, 175, 175);
    }
  }

  .menu-toggle-wrap {
    display: flex;
    justify-content: flex-end;
    margin-bottom: 1rem;

    position: relative;
    top:0;
    transition: 0.2s ease-out;

    .menu-toggle {
      transition: 0.2s ease-out;

      img {
        width: 2rem;
        // background-color: rgb(190, 175, 175);
        transition: 0.2s ease-out;
      }

      &:hover {
        img {
          background: var(--primary);
          transform: translateX(0.5rem);
        }
      }
    }
  }

h3, .button .text {
  opacity: 1;
  transition: 0.3s ease-out;
}

h3 {
    color: var(--grey);
    font-size: 0.875rem;
    margin-bottom: 0.5rem;
    text-transform: uppercase;
}
  .menu {
    margin: 0 -1rem;

    .button {
      display: flex;
      // justify-content: space-between;
      align-items: center;
      text-decoration: none;

      padding: 0.5rem 1rem;
      transition: 0.2s ease-out;

      img {
        width: 2rem;
        color: var(--light);
        margin-right: 1rem;
        transition: 0.2s ease-out;
      } 

      &:hover, &.router-link-exact-active {
        background-color: var(--dark-alt);

        img, .text {
          color: var(--primary);
        }
      }

      &.router-link-exact-active {
        border-right: 5px solid var(--primary);
      }

      .text {
        transition: 0.2s ease-out;
        color: var(--light);
      }

      &:hover {
        background: var(--dark-alt);

        img, .text {
          color: var(--primary);
        }
      }
    }
  }
  &.is-expanded {
    width: var(--sidebar-width);

    .menu-toggle-wrap {
      // top: -3rem;
      .menu-toggle {
        transform: rotate(-180deg)
      }
    }

    h3, button .text {
      opacity: 1;
    }
    .button {
      img {
        margin-right:
 1rem;
        
      }
    }
  }

  @media (max-width: 768px) {
    position: fixed;
    z-index: 99;

  }
}

</style> 

 

