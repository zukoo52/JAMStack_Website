<template>
  <div>
    <nuxt-content :document="pagecontent"  />
    <div>
      <nuxt />
    </div>
  </div>
</template>

<script>
export default {
layout:'newDefault',

data(){
return{
pagecontent: {},
};
},

async fetch(){
  this.pagecontent = await this.$content('my-team').fetch();
},

head(req){
  const ret = {}

  ret.title = this.pagecontent.title
  ret.meta =[]
  if(this.pagecontent.description !== undefined){
    ret.meta.push({
      hid: 'description',
    name: 'description',
    content:this.pagecontent.description,
    })
  }
  if(this.pagecontent.keywords !== undefined){
    ret.meta.push({
      hid: 'keywords',
    name: 'keywords',
    content:this.pagecontent.keywords,
    })
  }

  return ret
},

}

</script>

<style>

</style>
