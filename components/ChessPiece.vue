<template>
  <div class="chess_piece" @click="active=!active">
    <vs-tooltip>
      <vs-avatar circle size="300" color="#b64935">
        <img :src="require(`~/assets/images/${id}.png`)" alt="" />
      </vs-avatar>
      <template #tooltip>
        {{label}}
      </template>
    </vs-tooltip>
    <vs-dialog v-model="active">
      <template #header>
        <h4 class="not-margin">
          Bạn có muốn đặt <strong style="color: #b64935;">{{label}}</strong> ?
        </h4>
      </template>

      <div class="con-content">
        <vs-input border warn type="number" v-model="value" :step="1000" :min="1000" label-placeholder="Quất ngay với số tiền">
          <template #icon>
            <i class='bx bxs-badge-dollar' ></i>
          </template>
        </vs-input>
      </div>

      <template #footer>
        <div class="con-footer">
          <vs-button @click="active=false" transparent>
            Quất Luôn
          </vs-button>
          <vs-button @click="active=false" dark transparent>
            Thôi không đặt nữa
          </vs-button>
        </div>
      </template>

    </vs-dialog>
  </div>
</template>

<script>
export default {
  props: {
    id: {
      type: String,
    },
    label: {
      type: String
    }
  },
  data() {
    return {
      active: false,
      value: 0,
    }
  },
};
</script>
 <style lang="stylus">
  getColor(vsColor, alpha = 1)
      unquote("rgba(var(--vs-"+vsColor+"), "+alpha+")")
  getVar(var)
      unquote("var(--vs-"+var+")")
 .chess_piece 
    width: 300px
    margin-right: 16px
    margin-bottom: 16px
    cursor: pointer;
  .con-footer
    display flex
    align-items center
    justify-content flex-end
    .vs-button
      margin 0px
      .vs-button__content
        padding 10px 30px
      ~ .vs-button
        margin-left 10px
  .not-margin
    margin 0px
    font-weight normal
    padding 10px
    padding-bottom 0px
  .con-content
    width 100%
    p
      font-size .8rem
      padding 0px 10px
    .vs-checkbox-label
      font-size .8rem
    .vs-input-parent
      width 100%
    .vs-input-content
      margin 10px 0px
      width calc(100%)
      .vs-input
        width 100%
  .footer-dialog
    display flex
    align-items center
    justify-content center
    flex-direction column
    width calc(100%)
    .new
      margin 0px
      margin-top 20px
      padding: 0px
      font-size .7rem
      a
        color getColor('primary') !important
        margin-left 6px
        &:hover
          text-decoration underline
    .vs-button
      margin 0px
</style>

