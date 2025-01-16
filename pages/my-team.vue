<template>
  <div>
    <h1>this is the team page</h1>
    <div>
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
layout:'newDefault',
head(req){
  const ret = {}
  ret.title = "Team Info"
  return ret
},

}

</script>

<style>

</style>
