<script>
	import { goto } from '$app/navigation';
	let title = '';

	const addSuji = async () => {
		if (!title) {
			alert('筋を入力してください');
			return;
		}

		await fetch('http://localhost:8000/api/suji', {
			method: 'POST',
			headers: {
				'Content-Type': 'application/json'
			},
			body: JSON.stringify({ title })
		});
		goto('/suji');
	};
</script>

<body>
	<h1 class="takuann">Suji</h1>
	<div class="container">
		<div class="input-group">
			<input type="text" class="form-control" placeholder="筋を入力" bind:value={title} />
		</div>
		<button type="button" class="footer p-3 btn btn-danger mt-2" on:click={addSuji}
			>筋を追加する</button
		>
	</div>

	<footer class="footer fixed-bottom d-flex justify-content-around align-items-center">
		<a href="/suji" class="btn">💪</a>
		<a href="/suji2" class="btn"> ＋ </a>
		<a href="/suji3" class="btn">✏️</a>
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
