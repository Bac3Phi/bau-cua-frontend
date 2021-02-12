<template>
  <div style="padding: 64px;">
    <div class="grid">
      <vs-row>
        <vs-col :sm="12" :w="7">
          <chess-pieces :chessData="ChessPiecesData"/>
        </vs-col>
        <vs-col :sm="12" :w="5">
          <result-request :chessData="ChessPiecesData" />
          <result-table />
        </vs-col>
      </vs-row>
    </div>
  </div>
</template>
<script>
import ChessPieces from "../components/ChessPieces.vue";
import ResultRequest from '../components/ResultRequest.vue';
import ResultTable from "../components/ResultTable.vue";
import ResultTimer from "../components/ResultTimer.vue";
export default {
  components: { ChessPieces, ResultTable, ResultTimer, ResultRequest },
  data() {
    return {
      ChessPiecesData: [
        {
          id: "con_huou",
          label: "Con Hươu"
        },
        {
          id: "trai_bau",
          label: "Trái Bầu"
        },
        {
          id: "con_ga",
          label: "Con Gà"
        },
        {
          id: "con_ca",
          label: "Con Cá"
        },
        {
          id: "con_cua",
          label: "Con Cua"
        },
        {
          id: "con_tom",
          label: "Con Tôm"
        }
      ]
    };
  }
};
</script>
