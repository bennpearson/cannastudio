<template>
  <div class="cs-service">
    <h3 class="cs-service__title">
      {{ items.title }}
    </h3>
    <p class="cs-service__desc">
      {{ items.desc }}
    </p>
    <ul class="cs-service__projects">
      <li
        v-for="(item, index) in items.examples"
        :key="index"
        class="cs-service__project"
      >
        <div class="cs-service__logo" :class="'cs-service__logo--' + item.logo">
          <SvgPathIcon :name="item.logo" />
        </div>
        <h4 class="cs-service__project-title">
          {{ item.title }}
        </h4>
        <p class="cs-service__project-desc">
          {{ item.desc }}
        </p>
      </li>
    </ul>
  </div>
</template>

<script>
import SvgPathIcon from '~/components/SvgPathIcon.vue'

export default {
  components: {
    SvgPathIcon
  },
  props: {
    items: {
      type: Object,
      default: null
    }
  }
}
</script>

<style scoped>
.cs-service {
  padding: 20px 50px;
}
@media (min-width: 768px) {
  .cs-service {
    padding: 20px 100px;
  }
}
.cs-service__title {
  font-size: 36px;
  font-weight: normal;
  margin-bottom: 21px;
  line-height: 1;
}
@media (min-width: 768px) {
  .cs-service__title {
    font-size: 60px;
  }
}
.cs-service__desc {
  font-size: 18px;
  font-weight: normal;
  margin-bottom: 28px;
  max-width: 768px;
  line-height: 1.333;
}
@media (min-width: 768px) {
  .cs-service__desc {
    font-size: 28px;
  }
}
.cs-service__projects {
  display: flex;
  justify-content: space-between;
  flex-direction: column;
  list-style-type: none;
  margin: 0 0 50px -50px;
  padding: 0;
  max-width: 980px;
}
@media (min-width: 768px) {
  .cs-service__projects {
    flex-direction: row;
    margin: 0 0 50px -50px;
  }
}
.cs-service__project {
  position: relative;
  background-color: #15151b;
  padding: 200px 50px 50px 50px;
  margin-right: 0px;
  margin-bottom: 20px;
  width: 100%;
}
@media (min-width: 768px) {
  .cs-service__project {
    margin-right: 20px;
    width: 50%;
  }
}
.cs-service__logo {
  width: 100px;
  max-height: 110px;
  position: absolute;
  top: 50px;
  left: 50px;
}
.cs-service__logo--logo-crown {
  width: 120px;
}
.cs-service__logo--logo-bbc {
  width: 200px;
}
.cs-service__logo svg {
  width: 100%;
  height: auto;
  fill: white;
}
.cs-service__project-title {
  font-size: 24px;
  line-height: 1.125;
  margin-bottom: 18px;
  font-weight: normal;
}
.cs-service__project-desc {
  font-size: 16px;
  line-height: 1.5;
}
</style>
