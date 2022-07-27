<template>
  <nav>
    <div class="logo-container">
      <a href="#"><span class="logo">Baza</span></a>
    </div>
    <div class="menu-container mobile">
      <div class="hamburger-menu" @click="toggleDropdown" :class="{active: showMenu}">
        <div class="bar-top"></div>
        <div class="bar-middle"></div>
        <div class="bar-bottom"></div>
      </div>

      <div class="mobile-nav" :class="{active: showMenu}">
        <ul>
          <li>
            <a href="#">Shop</a>
          </li>
          <li>
            <a href="#">Sell Online</a>
          </li>
          <li>
            <a href="#">Blog</a>
          </li>
          <li>
            <a href="#">Contact Us</a>
          </li>
          <li>
            <button type="button">Buy Now</button>
          </li>

        </ul>
      </div>
    </div>

    <div class="menu-container desktop">
      <ul>
        <!-- <a href="#">Shop</a> -->
        <MenuItem item-title="Shop" item-link="#" :dropdown-items="[]" />

        <MenuItem
          item-title="Sell Online"
          item-link="#"
          :dropdown-items="[
            { title: 'My account', url: '#' },
            { title: 'Cart', url: '#' },
            { title: 'Checkout', url: '#' },
          ]"
        />

        <MenuItem
          item-title="Blog"
          item-link="#"
          :dropdown-items="[
            { title: 'Blog One Column', url: '#' },
            { title: 'Blog One Column With Sidebar', url: '#' },
            { title: 'Blog One Column', url: '#' },
            { title: 'Blog One Column With Sidebar', url: '#' },
          ]"
        />

        <MenuItem
          item-title="Contact Us"
          item-link="#"
          :dropdown-items="[
            { title: 'Contact Us 1', url: '#' },
            { title: 'Contact Us 2', url: '#' },
            { title: 'Contact Us 3', url: '#' },
            { title: 'Contact Us 4', url: '#' },
          ]"
        />

        <li>
          <button type="button">Buy Now</button>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
import MenuItem from "../widgets/MenuItem.vue";

export default {
  name: "NavBar",
  components: {
    MenuItem,
  },
  data() {
    return {
      showMenu: false
    }
  },
  methods: {
    toggleDropdown() {
      this.showMenu = !this.showMenu;
    }
  }
};
</script>

<style lang="scss" scoped>
@media screen and (min-width: 768px) {
  nav {
    display: grid;
    grid-template-columns: auto 1fr;
    height: 6rem;
    padding: 1.6rem;
    max-width: 1700px;
    margin: 0 auto;

    .logo-container {
      align-self: center;

      .logo {
        font-weight: 800;
        font-size: 1.875rem;
      }
    }

    .menu-container {
      align-self: center;

      &.mobile {
        display: none;
      }

      ul {
        list-style: none;
        display: flex;
        justify-content: end;
        align-items: center;

        li {
          button {
            font-weight: 500;
            padding: 0.6rem 1.6rem;
            border: 0.5px solid rgba(84, 89, 95, 0.5);
            border-radius: 1rem;
            background-color: var(--background);
            color: #000;
            margin-left: 1.4rem;
            transition: color 0.3s, background 0.3s;

            &:hover {
              background-color: #000;
              color: #fff;
            }
          }
        }
      }
    }
  }
}

@media screen and (max-width: 768px) {
  nav {
    display: grid;
    grid-template-columns: min-content min-content;
    height: 6rem;
    padding: 1.6rem;
    justify-content: space-between;
    max-width: 1700px;
    margin: 0 auto;

    .logo-container {
      align-self: center;

      .logo {
        font-weight: 800;
        font-size: 1.875rem;
      }
    }

    .menu-container {
      align-self: center;

      &.desktop {
        display: none;
      }

      .hamburger-menu {
        display: flex;
        flex-flow: column wrap;
        justify-content: space-between;
        height: 2.5rem;
        width: 2.5rem;
        cursor: pointer;
        position: relative;
        z-index: 999;

        .bar-top,
        .bar-middle,
        .bar-bottom {
          height: 5px;
          background: var(--dark);
          border-radius: 5px;
          margin: 3px 0;
          transform-origin: left;
          transition: all 0.5s;
        }

        &.active {
          position: fixed;
          top: 30px;
          right: 20px;

          .bar-top {
            transform: rotate(48deg);
          }
          .bar-middle {
            transform: translateX(1rem);
            opacity: 0;
          }

          .bar-bottom {
            transform: rotate(-48deg);
          }
        }
      }

      .mobile-nav {
        z-index: 998;
        position: fixed;
        width: 100%;
        height: 100%;
        background-color: #fff;
        left: 0;
        top: 0;
        overflow: hidden;
        border-top: solid 8px var(--primary);

        pointer-events: none;
        opacity: 0;

        transition: opacity 0.2s;

        &.active {
          pointer-events: all;
          opacity: 1;
        }

        ul {
          list-style: none;
          display: flex;
          flex-direction: column;
          justify-content: center;
          height: 100%;

          li {
            text-align: center;

            a {
              font-weight: 700;
              padding: 0.875rem 1.2rem;
              width: 100%;
              display: inline-block;
              font-size: 1.8rem;
            }
            
            button {
              margin-top: 2rem;
              font-weight: 500;
              padding: 0.6rem 1.6rem;
              border: 0.5px solid rgba(84, 89, 95, 0.5);
              border-radius: 1rem;
              background-color: var(--background);
              color: #000;
              transition: color 0.3s, background 0.3s;

              &:hover {
                background-color: #000;
                color: #fff;
              }
            }
          }
        }
      }
    }
  }
}
</style>
