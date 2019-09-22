<template>
  <div class="cs-header">
    <div class="cs-header__content">
      <h1 class="cs-header__title">
        {{ title }}
      </h1>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: null
    }
  }
}
</script>

<style scoped>
.cs-header {
  margin: 60px 50px 0px 50px;
}
@media (min-width: 768px) {
  .cs-header {
    margin: 60px 100px 0px 100px;
  }
}
.cs-header__content {
  display: inline-block;
  padding: 16px;
  border: 1px solid white;
}
@media (min-width: 768px) {
  .cs-header__content {
    padding: 20px;
  }
}
.cs-header__title {
  color: white;
  text-transform: uppercase;
  font-weight: 300;
  letter-spacing: 6px;
  font-size: 21px;
  line-height: 1.125;
}
@media (min-width: 768px) {
  .cs-header__title {
    font-size: 36px;
  }
}
</style>
