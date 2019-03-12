<template>
  <ul class="home">
    <li v-for="(item,index) in images" :key="index" @click="preview(index)">
      <img :src="item" alt="">
    </li>
  </ul>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'home',
  data(){
    return {
      images:[
        'https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1552307885259&di=816e9dd1a8eb6635f3924fc38fc7b4a3&imgtype=0&src=http%3A%2F%2Fh.hiphotos.baidu.com%2Fimage%2Fpic%2Fitem%2F730e0cf3d7ca7bcb051bd704b0096b63f624a8bc.jpg',
        'https://ss1.baidu.com/9vo3dSag_xI4khGko9WTAnF6hhy/image/h%3D300/sign=a573495ce5f81a4c3932eac9e72a6029/2e2eb9389b504fc27c224b2debdde71190ef6d9d.jpg',
        'https://ss1.baidu.com/-4o3dSag_xI4khGko9WTAnF6hhy/image/h%3D300/sign=6782f9d0db6285358de0d421a0ee76f2/6609c93d70cf3bc763ef4ecedf00baa1cd112a21.jpg'
      ]
    }
  },
  methods: {
    preview(index) {
      this.$imagePreview({
        images: this.images,
        index: index,
        defaultOpt: {
          fullscreenEl: true,
          shareEl: false,
          arrowEl: true,
          preloaderEl: true,
          loop: false,
          bgOpacity: 0.85,
          showHideOpacity: true,
          errorMsg: '<div class="pswp__error-msg">图片加载失败</div>',
        }
      })
    }
  }
}
</script>
<style lang="scss">
img{
  width: 100%;
}

</style>


