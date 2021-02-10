<template>
  <div class="hidden">
    <vs-sidebar absolute hover-expand reduce v-model="active" open>
      <template #logo>
      </template>
        <vs-sidebar-item id="home" to="/">
          <template #icon>
            <i class='bx bx-dice-6' ></i>
          </template>
          Đá Bi
        </vs-sidebar-item>
      <vs-sidebar-item id="history" to="history">
        <template #icon>
          <i class="bx bx-history"></i>
        </template>
        Lịch Sử Bet Bủng
      </vs-sidebar-item>
      <vs-sidebar-item id="payment" to="payment">
        <template #icon>
          <i class='bx bx-credit-card-alt' ></i>
        </template>
        Thanh Toán
      </vs-sidebar-item>

      <template #footer>
        <vs-sidebar-item id="logout">
          <template #icon>
            <i class="bx bx-log-out"></i>
          </template>
          Sign Out
        </vs-sidebar-item>
      </template>
    </vs-sidebar>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: "home",
    }
  },
};
</script>
