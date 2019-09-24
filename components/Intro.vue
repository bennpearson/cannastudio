<template>
  <div class="cs-intro">
    <h2 class="cs-intro__title">
      {{ subtitle }}
    </h2>
    <a class="cs-intro__mailto" href="mailto:hello@cannastudio.co.uk">
      Contact us
    </a>
  </div>
</template>

<script>
export default {
  props: {
    subtitle: {
      type: String,
      default: null
    }
  }
}
</script>

<style scoped>
.cs-intro {
  margin-bottom: 100px;
}
@media (min-width: 768px) {
  .cs-intro {
    margin-bottom: 160px;
  }
}
.cs-intro__title {
  font-size: 50px;
  color: white;
  font-weight: normal;
  padding: 50px 50px 70px 50px;
  max-width: 1300px;
  line-height: 1.125;
}
@media (min-width: 768px) {
  .cs-intro__title {
    font-size: 100px;
    padding: 100px 100px 130px 100px;
  }
}
.cs-intro__mailto {
  color: black;
  background-color: white;
  font-size: 18px;
  padding: 10px 25px;
  margin: 0 50px;
  font-weight: bold;
  cursor: pointer;
  text-decoration: none;
  display: inline-block;
}
@media (min-width: 768px) {
  .cs-intro__mailto {
    font-size: 28px;
    padding: 20px 50px;
    margin: 0 100px;
  }
}
</style>
