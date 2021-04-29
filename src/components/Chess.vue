<template>
	<div id="board1"></div>
</template>

<script>
import ChessBoard from "chessboardjs-vue";
export default {
	data() {
		return {
			config: {
				draggable: true,
				dropOffBoard: "snapback", // this is the default
				position: "start",
			},
		};
	},
	name: "Home",
	components: { ChessBoard },

	mounted() {
		ChessBoard("board1", this.config);
	},
};
</script>

<style>
#board1 {
	width: 400px;
}
</style>
