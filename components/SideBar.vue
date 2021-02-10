<template>
  <div class="hidden">
    <vs-sidebar absolute hover-expand reduce v-model="active" open>
      <template #logo>
        <!-- ...img logo -->
      </template>
      <vs-sidebar-item id="home">
        <template #icon>
          <i class="bx bx-home"></i>
        </template>
        Home
      </vs-sidebar-item>
      <vs-sidebar-item id="history">
        <template #icon>
          <i class="bx bx-history"></i>
        </template>
        History
      </vs-sidebar-item>

      <template #footer>
        <vs-row justify="space-between">
          <vs-avatar badge-color="danger" badge-position="top-right">
            <i class="bx bx-bell"></i>

            <template #badge>
              28
            </template>
          </vs-avatar>

          <vs-avatar>
            <img src="/avatars/avatar-5.png" alt="" />
          </vs-avatar>
        </vs-row>
      </template>
    </vs-sidebar>
  </div>
</template>

<script>
export default {};
</script>
