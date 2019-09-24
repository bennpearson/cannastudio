<template>
  <footer class="cs-footer">
    <h4 class="cs-footer__title">
      {{ footer.title }}
    </h4>
    <p class="cs-footer__desc">
      {{ footer.desc }}
    </p>
  </footer>
</template>

<script>
export default {
  props: {
    footer: {
      type: Object,
      default: null
    }
  }
}
</script>

<style scoped>
.cs-footer {
  padding: 50px;
  background-color: white;
}
@media (min-width: 768px) {
  .cs-footer {
    padding: 100px;
  }
}
.cs-footer__title {
  color: black;
  font-size: 36px;
  font-weight: normal;
  margin-bottom: 21px;
  line-height: 1;
}
@media (min-width: 768px) {
  .cs-footer__title {
    font-size: 60px;
  }
}
.cs-footer__desc {
  color: black;
  font-size: 18px;
  font-weight: normal;
  margin-bottom: 28px;
  max-width: 768px;
  line-height: 1.333;
}
@media (min-width: 768px) {
  .cs-footer__desc {
    font-size: 28px;
  }
}
</style>
