<template>
  <div id="Game-view">
    <div id="Game-info">{{status}}</div>
    <div id="Game-squares">
      <div
        v-for="(square,index) in table.squares"
        v-bind:key="square"
        v-bind:class="{hilighted :square.isHilighted}"
        @click="clicked({index})"
        class="game-view-squares"
      >{{square.value? square.value :'⠀'}}</div>
    </div>
  </div>
</template>


<script>
import { Game } from "../script/Game";
const table = new Game();
export default {
  name: "Game-view",
  data() {
    return { table: table };
  },
  computed: {
    status: () => {
      if (table.inProgress) {
        return `It is ${table.currentTurn} turn.`;
      } else if (table.winner) {
        return `${table.winner} wins`;
      } else {
        return `Tie`;
      }
    }
  },
  methods: {
    clicked: i => {
      table.makeMove(i.index);
    }
  }
};
</script>

<style scoped>
#Game-view {
  width: 70%;
  margin: 0 auto;
  border: 2px solid rgba(63, 63, 63, 0.767);
}
#Game-info {
  padding: 15px;
  font-family: sans-serif;
  font-size: 20px;
  font-weight: bold;
  text-align: center;
}
#Game-squares {
  height: 80%;
  display: flex;
  flex-wrap: wrap;
  padding: 2%;
  box-sizing: border-box;
}
.game-view-squares {
  width: 33.33%;
  height: 33.33%;

  display: flex;
  justify-content: center;
  align-content: center;
  box-sizing: border-box;

  font-family: cursive;
  padding: 10%;
  font-size: 200%;
  text-transform: uppercase;

  cursor: pointer;
  user-select: none;
  -moz-user-select: none;
}
.game-view-squares.hilighted {
  background-color: rgba(0, 128, 0, 0.274);
}
.game-view-squares:hover {
  background-color: #eee;
}
.game-view-squares:nth-child(-n + 6) {
  border-bottom: 3px solid rgba(4, 8, 238, 0.281);
}
.game-view-squares:nth-child(3n + 1) {
  border-right: 3px solid rgba(4, 86, 238, 0.281);;
}
.game-view-squares:nth-child(3n + 2) {
  border-right: 3px solid rgba(4, 86, 238, 0.281);;
}
</style>