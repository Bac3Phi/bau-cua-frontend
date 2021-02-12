<template>
<div style="background: white; margin-bottom: 16px; padding: 16px; border-radius: 8px">
  <vs-button @click="handleCreateUser">Thêm người đặt</vs-button>
    <vs-table>
      <template #thead>
        <vs-tr>
          <vs-th>
            ID
          </vs-th>
          <vs-th>
            Người đặt
          </vs-th>
          <vs-th>
            Linh Vật
          </vs-th>
          <vs-th>
            Money
          </vs-th>
        </vs-tr>
      </template>
      <template #tbody>
        <vs-tr :key="i" v-for="(tr, i) in users" :data="tr">
          <vs-td>
            {{ tr.id }}
          </vs-td>
          <vs-td
            edit
            @click="(edit = tr), (editProp = 'name'), (editActive = true)"
          >
            {{ tr.name }}
          </vs-td>
          <vs-td
            edit
            @click="(edit = tr), (editProp = 'animal'), (editActive = true)"
          >
            {{ tr.animal }}
          </vs-td>
          <vs-td
            edit
            @click="(edit = tr), (editProp = 'money'), (editActive = true)"
          >
            {{ tr.money }}
          </vs-td>
        </vs-tr>
      </template>
    </vs-table>

    <vs-dialog v-model="editActive">
      <template #header> Change Prop {{ editProp }} </template>
      <vs-input
        @keypress.enter="editActive = false"
        v-if="editProp == 'name'"
        v-model="edit[editProp]"
      />
      <vs-input
        @keypress.enter="editActive = false"
        v-if="editProp == 'animal'"
        v-model="edit[editProp]"
      />
      <vs-select
        @change="editActive = false"
        block
        v-if="editProp == 'animal'"
        placeholder="Select"
        v-model="edit[editProp]"
      >
        <vs-option label="Con Hươu" value="Con Hươu">
          Con Hươu
        </vs-option>
        <vs-option label="Trái Bầu" value="Trái Bầu">
          Trái Bầu
        </vs-option>
        <vs-option label="Con Gà" value="Con Gà">
          Con Gà
        </vs-option>
        <vs-option label="Con Cá" value="Con Cá">
          Con Cá
        </vs-option>
        <vs-option label="Con Cua" value="Con Cua">
          Con Cua
        </vs-option>
        <vs-option label="Con Tôm" value="Con Tôm">
          Con Tôm
        </vs-option>
      </vs-select>
    </vs-dialog>
  </div>
</template>
<script>
export default {
  data: () => ({
    editActive: false,
    edit: null,
    editProp: {},
    users: []
  }),
  methods: {
    handleCreateUser(e) {
      this.users.push({
        id: this.lastId,
        name: "Nguyễn Văn A",
        animal: "",
        money: ""
      },)
    }
  },
  computed: {
    lastId() {
      return this.users.length  
    }
  },
};
</script>
