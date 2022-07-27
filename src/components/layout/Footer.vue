<template>
  <footer>
    <div class="container-footer">
      <div class="copyright">
        <span
          >Copyright ©{{ new Date().getFullYear() }} Baza. All rights
          reserved.</span
        >
      </div>
      <div class="menu-container">
        <ul>
          <li>
            <a href="#">What's New</a>
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
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterSection",
};
</script>

<style lang="scss" scoped>
footer {
  background-color: #f8f9fa;

  .container-footer {
    display: grid;
    grid-template-columns: repeat(auto-fill, 100%);
    height: 100%;
    padding: 1.6rem;
    max-width: 1700px;
    margin: 0 auto;
    margin-top: 5rem;

    .copyright {
      text-align: center;
      margin-top: 1rem;
      align-self: center;

      span {
        color: var(--text-body);
      }
    }

    @media screen and (min-width: 768px) {
      grid-template-columns: 1fr 1fr;
      height: 6rem;

      .copyright {
        text-align: left;
        margin-top: 0;
      }
    }

    .menu-container {
      align-self: center;

      @media screen and (max-width: 768px) {
        grid-row: 1;

        ul {
          list-style: none;
          display: flex;
          justify-content: end;
          align-items: center;
          gap: 1rem;
          flex-direction: column;
          padding: 1rem 0;

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

      @media screen and (min-width: 768px) {
        ul {
          list-style: none;
          display: flex;
          justify-content: end;
          align-items: center;
          gap: 3rem;

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
}
</style>
