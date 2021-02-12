<template>
  <div style="display: flex; max-width: 1000px; flex-flow: wrap;">
    <chess-piece
      v-for="chess in chessData"
      :key="chess.key"
      :id="chess.id"
      :label="chess.label"
    />
  </div>
</template>

<script>
import ChessPiece from "./ChessPiece.vue";

export default {
  components: { ChessPiece },
  props: {
    chessData: {
      type: Array,
    },
  },
};
</script>

<style scoped></style>
