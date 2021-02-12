<template>
  <div style="padding: 64px">
    <div class="grid">
      <vs-row>
        <vs-col :sm="12" :w="7">
          <vs-button size="xl" @click="handleCreateResult"> Start </vs-button>
        </vs-col>
      </vs-row>

      <vs-row>
        <vs-col :sm="12" :w="7">
          <chess-pieces />
        </vs-col>
        <vs-col :sm="12" :w="5">
          <!-- <result-timer /> -->
          <result-table />
        </vs-col>
      </vs-row>
    </div>
  </div>
</template>

<script>
import ChessPieces from "../components/ChessPieces.vue";
import ResultTable from "../components/ResultTable.vue";
import ResultTimer from "../components/ResultTimer.vue";

export default {
  methods: {
    handleCreateResult() {
      return ["con_huou", "trai_bau", "con_ga", "con_ca", "con_cua", "con_tom"]
        .sort(() => 0.5 - Math.random())
        .slice(0, 3);
    },
  },
  components: { ChessPieces, ResultTable, ResultTimer },
};
</script>
