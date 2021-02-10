<template>
  <div style="padding: 64px;">
    <div
      class="center"
      style="background: white; margin-bottom: 16px; padding: 16px; border-radius: 8px"
    >
      <h1>Nạp Card Time</h1>
      <div style="margin-top: 32px;">
        <vs-row>
          <vs-col :w="4">
            <vs-select filter placeholder="Filter" label="Label" v-model="value">
              <vs-option label="Vuesax" value="1">
                Vuesax
              </vs-option>
              <vs-option label="Vue" value="2">
                Vue
              </vs-option>
              <vs-option label="Javascript" value="3">
                Javascript
              </vs-option>
              <vs-option label="Sass" value="4">
                Sass
              </vs-option>
              <vs-option label="Typescript" value="5">
                Typescript
              </vs-option>
              <vs-option label="Webpack" value="6">
                Webpack
              </vs-option>
              <vs-option label="Nodejs" value="7">
                Nodejs
              </vs-option>
            </vs-select>
          </vs-col>
          <vs-col :w="1"></vs-col>
          <vs-col :w="4"> 
            <vs-input type="number" label="Number" 
              class="bc-number-input"/>
          </vs-col>
          <vs-col :w="1"></vs-col>
          <vs-col :w="2">
            <vs-button
              icon
              color="danger"
              border
              :active="active == 2"
              @click="active = 2"
            >
              <i class='bx bxs-heart' ></i>
            </vs-button>
          </vs-col>
        </vs-row>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    value: ""
  })
};
</script>
<style lang="stylus">
.bc-number-input
  input.vs-input
    width: 100%
    height 38px
.vs-select-content
  max-width inherit
</style>
