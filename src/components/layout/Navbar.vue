<template>
  <nav>
    <div class="logo-container">
        <a href="#"><span class="logo">Baza</span></a>
    </div>
    <div class="menu-container">
        <ul>
            <!-- <a href="#">Shop</a> -->
            <MenuItem item-title="Shop" item-link="#" :dropdown-items="[]" />

            <MenuItem item-title="Sell Online" item-link="#" :dropdown-items="[{title: 'My account', url: '#'}, {title: 'Cart', url: '#'}, {title: 'Checkout', url: '#'}]"/>

            <MenuItem item-title="Blog" item-link="#" :dropdown-items="[{title: 'Blog One Column', url: '#'}, {title: 'Blog One Column With Sidebar', url: '#'}, {title: 'Blog One Column', url: '#'}, {title: 'Blog One Column With Sidebar', url: '#'}]"/>

            <MenuItem item-title="Contact Us" item-link="#" :dropdown-items="[{title: 'Contact Us 1', url: '#'}, {title: 'Contact Us 2', url: '#'}, {title: 'Contact Us 3', url: '#'}, {title: 'Contact Us 4', url: '#'}]"/>
            
            <li>
                <button type="button">Buy Now</button>
            </li>
        </ul>
    </div>
  </nav>
</template>

<script>

import MenuItem from '../widgets/MenuItem.vue'

export default {
  name: 'NavBar',
  components: {
      MenuItem
  }
}
</script>

<style lang="scss" scoped>

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

</style>
