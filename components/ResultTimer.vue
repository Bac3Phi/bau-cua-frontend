<template>
<div style="background: white; margin-bottom: 16px; padding: 16px; border-radius: 8px">
  <h1>Đã Quất</h1>
  <vs-table striped >
    <template #thead>
      <vs-tr>
        <vs-th>
          Name
        </vs-th>
        <vs-th>
          Email
        </vs-th>
        <vs-th>
          Id
        </vs-th>
      </vs-tr>
    </template>
    <template #tbody>
      <vs-tr :key="i" v-for="(tr, i) in users" :data="tr">
        <vs-td>
          {{ tr.name }}
        </vs-td>
        <vs-td>
          {{ tr.email }}
        </vs-td>
        <vs-td>
          {{ tr.id }}
        </vs-td>
      </vs-tr>
    </template>
  </vs-table>
</div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        {
          id: 1,
          name: "Leanne Graham",
          username: "Bret",
          email: "Sincere@april.biz",
          website: "hildegard.org"
        },
        {
          id: 2,
          name: "Ervin Howell",
          username: "Antonette",
          email: "Shanna@melissa.tv",
          website: "anastasia.net"
        },
        {
          id: 3,
          name: "Clementine Bauch",
          username: "Samantha",
          email: "Nathan@yesenia.net",
          website: "ramiro.info"
        },
        {
          id: 4,
          name: "Patricia Lebsack",
          username: "Karianne",
          email: "Julianne.OConner@kory.org",
          website: "kale.biz"
        },
        {
          id: 5,
          name: "Chelsey Dietrich",
          username: "Kamren",
          email: "Lucio_Hettinger@annie.ca",
          website: "demarco.info"
        },
      ]
    };
  }
};
</script>
