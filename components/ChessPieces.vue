<template>
  <div style="display: flex; max-width: 1000px; flex-flow: wrap;">
    <chess-piece
      v-for="chess in ChessPiecesData"
      :key="chess.key"
      :id="chess.id"
      :label="chess.label"
    />
  </div>
</template>

<script>
import ChessPiece from "./ChessPiece.vue";
const ChessPiecesData = [
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
];
export default {
  components: { ChessPiece },
  data() {
    return {
      ChessPiecesData
    };
  }
};
</script>

<style scoped></style>
