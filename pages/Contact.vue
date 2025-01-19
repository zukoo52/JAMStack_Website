<template>
  <div>
   <nuxt-content :document="pagecontent"  />
  </div>
</template>

<script>
export default {
layout: 'newDefault',

data(){
  return{
    pagecontent: {},
  };
},
// Fetch the main.md content
async fetch(){
this.pagecontent = await this.$content('contact').fetch();
},
head (req){
const ret = {}

ret.title = this.pagecontent.title // in here using .md file and get the title from that page
ret.meta = [] // using .md file to SEO
if(this.pagecontent.description !== undefined){
  ret.meta.push({
    hid: 'description',
    name: 'description',
    content:this.pagecontent.description,
  })
}
if(this.pagecontent.keywords !== undefined) // using .md file to SEO
{
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
