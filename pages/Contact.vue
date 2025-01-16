<template>
  <div>

    <section class="Heading">
      <h1> Contact US</h1>
    </section>




    <div class="layouts">
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
layout: "newDefault",
head(req){
  const ret = {}
  ret.title = "Contact US"
  return ret
},
}
</script>

<style>

</style>
