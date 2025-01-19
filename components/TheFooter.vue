<template>
  <footer>
  <div class="footer-content">
    <div></div>
    <div>&copy;2022 MY Company</div>

    <NuxtLink to="/mainPage">
      <p  class="logo-details">
        {{ $store.state.siteproperties.sitename}}
      </p >
    </NuxtLink>
  </div>
</footer>
</template>

<script>
export default {

}
</script>

<style>
footer{
  margin-top: auto;
  background-color: antiquewhite;
}
.footer-content{
  margin: 1em 0;
  display: flex;
  justify-content: space-between;
}

</style>
