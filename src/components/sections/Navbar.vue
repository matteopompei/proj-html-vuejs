<template>
  <section>
    <div class="container">
      <img
        src="../../assets/img/avada-drivers-logo-1x.png"
        alt="Avada Driving School"
      />
      <nav>
        <ul>
          <li v-for="(element, index) in menu" :key="index">
            <a
              href="#"
              :class="{
                active: element.isActive,
                new: element.isNew,
                button: element.lastItem,
              }"
              >{{ element.text }}</a
            >
          </li>
        </ul>
      </nav>
    </div>
  </section>
</template>

<script>
export default {
  name: "Navbar",
  props: {
    menu: Array,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/vars.scss";

section {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  padding: 30px 0;
  background: rgba(51, 51, 51, 0.4);

  nav {
    display: flex;
    align-items: center;

    ul {
      list-style: none;

      li {
        display: inline-block;
        margin: 0 20px;

        a {
          padding-bottom: 15px;
          font-size: 0.9rem;
          color: #fff;
          text-decoration: none;
          font-weight: bold;
          text-transform: uppercase;
          border-bottom: 2px solid transparent;
          transition: 0.5s;

          &:hover,
          &.active {
            color: $accent;
            border-bottom: 2px solid $accent;
          }

          &.button {
            padding: 13px 30px;
            border: none;

            &:hover {
              color: inherit;
              border-bottom: inherit;
            }
          }

          &.new::after {
            margin-left: 10px;
            padding: 2px 5px;
            content: "New";
            font-size: 0.7rem;
            text-transform: uppercase;
            background: $accent;
            border-radius: 3px;
          }
          &.new:hover {
            color: #fff;
          }
        }
      }
    }
  }
}
</style>
