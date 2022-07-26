<template>
    <li class="item-container">
        <a :href='itemLink'>{{ itemTitle }} &nbsp; <font-awesome-icon v-if="hasDropdown" icon="fas fa-chevron-down" size="2xs"/></a>
        <div v-if="hasDropdown" class="dropdown-container">
            <ul>
                <li>
                    <a href="#">Link 1</a>
                </li>
                <li>
                    <a href="#">Link 1</a>
                </li>
                <li>
                    <a href="#">Link 1</a>
                </li>
            </ul>
        </div>
    </li>

</template>

<script>
import { library } from '@fortawesome/fontawesome-svg-core'
import { faChevronDown } from '@fortawesome/free-solid-svg-icons'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'

library.add(faChevronDown);

export default {
  name: 'MenuItem',
  props: {
      itemTitle: String,
      itemLink: String,
      hasDropdown: Boolean
  },
  components:  {
    'font-awesome-icon': FontAwesomeIcon
  }
  
}
</script>

<style lang="scss" scoped>

li.item-container {
    font-weight: 600;
    position: relative;

    &:hover {
        .dropdown-container {
            pointer-events: all;
            opacity: 1;
            transform: translateY(0%);
        }

        a {
            color: var(--primary);

            > svg {
                transform: rotate(-180deg);
            }
        }
    }

    a {
        transition: color 0.2s;
        display: inline-block;
        padding: 1rem 1.2rem;

        & > svg {
            transition: transform 0.4s;
        }
    }

    .dropdown-container {
        position: absolute;
        width: 100%;
        top: 50px;
        left: 0px;
        z-index: 999;
        background: var(--background);
        border-top: solid 2px var(--primary);
        border-bottom-left-radius: 0.25rem;
        border-bottom-right-radius: 0.25rem;
        opacity: 0;
        transform: translateY(2%);
        pointer-events: none;
        box-shadow: 0 0 20px rgba(0,0,0,0.1);

        transition: opacity 0.2s, transform 0.2s;

        &:hover {
            opacity: 1;
            transform: translateY(0%);
        }

        ul {
            list-style: none;
            padding: 0.5rem;

            li a {
                padding: 0.875rem;
                width: 100%;
                display: inline-block;
                color: var(--secondary);
                background: var(--background);
                border-radius: 0.25rem;


                transition: color 0.2s, background 0.2s;

                &:hover {
                    color: var(--dark);
                    background-color: #f0f0f0;
                }
            }
        }
    }
}


</style>
