<template>
  <header class="cs-header">
    <div class="cs-header__content">
      <h1 class="cs-header__title">
        {{ title }}
      </h1>
    </div>
  </header>
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
  padding: 14px;
  border: 2px solid white;
}
@media (min-width: 768px) {
  .cs-header__content {
    padding: 20px;
    border: 4px solid white;
  }
}
.cs-header__title {
  color: white;
  text-transform: uppercase;
  font-weight: bold;
  letter-spacing: 6px;
  font-size: 21px;
  line-height: 1.125;
}
@media (min-width: 768px) {
  .cs-header__title {
    font-size: 42px;
  }
}
</style>
