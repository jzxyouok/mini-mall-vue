<template>
  <grid>
      <grid-item 
        v-for="item in shelfList"
        :label="item.name"
        :link="{ name: 'shelfProductPreview', params: { id: item.id }}">

        <img slot="icon" :src="item.cover_image">

      </grid-item>
  </grid>
</template>

<script>
    import {
        Grid,
        GridItem
    } from 'vux';
    export default {
        name: 'shelf',
        components: {
            Grid,
            GridItem
        },
        props: {
            shelfList: Array
        },
        methods: {
            // onItemClick () {
            //   console.log('去产品列表')
            // }
        }
    }
</script>

<style lang="less">

</style>