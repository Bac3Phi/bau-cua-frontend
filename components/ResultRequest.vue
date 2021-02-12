<template>
  <div style="padding: 30px; background: white; border-radius: 8px; margin-bottom: 16px">
    <vs-button
      relief
      block
      size="xl"
      @click="handleClick"
    >
      <i class="bx bxs-paper-plane"></i> Xỗ Nuôn
    </vs-button>
    <div ref="content" class="content-div">
      <div class="result-box" v-for="chess in randomData" :key="chess.id">
        <img :src="require(`~/assets/images/${chess.id}.png`)" width="200"/>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      chessData: {
        type: Array
      },
    },
    data() {
      return {
        isLoading: false,
        randomData: [],
      }
    },
    methods: {
      handleClick(e) {
        this.randomData = [];
        const loading = this.$vs.loading({
        })
        setTimeout(() => {
          for (let index = 0; index < 3; index++) {
           this.randomData.push(this.createResult())
          }

          loading.close()
        }, 1500)
      },
      createResult() {
        return this.chessData[Math.floor(Math.random() * this.chessData.length)];
      },
    },
  }
</script>
  <style scoped lang="stylus">
    .content-div
      display flex
      justify-content space-between
    .result-box
      width 200px
      height 200px
      position relative
      margin 5px
      border-radius 20px
      box-shadow 0px 10px 20px -10px rgb(0 0 0 / 52%)
      overflow hidden
      cursor pointer
      transition all .25s ease
      &:hover
        transform translate(0,-5px)
        box-shadow 0px 15px 20px -10px rgba(0,0,0,.09)
  </style>