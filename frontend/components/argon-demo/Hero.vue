<template>
  <section class="section-hero section-shaped my-0">
    <div class="shape shape-style-1 shape-primary">
      <span class="span-150" />
      <span class="span-50" />
      <span class="span-50" />
      <span class="span-75" />
      <span class="span-100" />
      <span class="span-75" />
      <span class="span-50" />
      <span class="span-100" />
      <span class="span-50" />
      <span class="span-100" />
    </div>
    <div class="container-fluid d-flex align-items-center">
      <div class="col px-0 mb-4">
        <div class="row justify-content-center align-items-center">
          <div class="col-lg-10 text-center pt-lg slider">
            <slot>
              <p class="lead text-white mt-4">
                A beautiful Design System for Bootstrap 4. It's Free and Open Source.
              </p>
            </slot>
          </div>
        </div>
        <div class="row align-items-center justify-content-around stars-coded">
          <div class="col-sm-10 mt-sm-0 text-right">
            <span class="text-white alpha-7 ml-3">{{ $t('index.vote') }}</span>
            <a href="https://github.com/sun-asterisk-research/air-visual" target="_blank" title="Support us on Github">
              <img src="/argon/img/brand/github-white-slim.png" alt="github" style="height: 22px; margin-top: -3px">
            </a>
          </div>
          <!-- <div class="col-sm-4 mt-4 mt-sm-0 text-right">
            <span class="text-white alpha-7">Coded by</span>
            <a href="https://github.com/sun-asterisk-research" target="_blank" title="R&D Open Source">
              <img src="/argon/img/brand/creativetim-white-slim.png" class="ml-3" style="height: 30px;">
            </a>
          </div> -->
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {}
</script>
<style lang="scss" scoped>
.section-hero {
  height: 100vh;
}
.slider {
  margin-top: 6em;
}
.stars-coded {
  margin-top: 10em;
}
</style>
