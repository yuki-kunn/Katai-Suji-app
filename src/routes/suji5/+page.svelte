<script>
</script>

<body>
	<h1 class="takuann">Suji</h1>
	<div class="container">
		<div class="input-group">
			<input type="text" class="form-control" placeholder="筋を入力" />
		</div>
		<button type="button" class="footer p-3 btn btn-danger mt-2">ToDoを追加する</button>
		<h1 class="takuann">筋を通せない</h1>
	</div>

	<footer class="footer fixed-bottom d-flex justify-content-around align-items-center">
		<button type="button" class="btn btn-outline-primary">💪</button>
		<button type="button" class="btn btn-outline-primary"> ＋ </button>
		<button type="button" class="btn btn-outline-primary">✏️</button>
	</footer>
</body>

<style>
	.takuann {
		text-align: center;
		color: red;
		margin-bottom: 11em;
	}

	.container {
		height: 10px;
		margin: 0 auto;
	}

	/* フッターの設定 */
	.footer {
		width: 100%;
		padding: 10px;
	}

	/* フッターのボタンのスタイル調整 */
	.footer button {
		border: none;
		background: none;
	}
</style>
