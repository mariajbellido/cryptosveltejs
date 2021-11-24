<script>

	let coins = []

	const loadCoins = async() => {
		const res = await fetch('https://api.coingecko.com/api/v3/coins/markets?vs_currency=eur&order=market_cap_desc&per_page=100&page=1&sparkline=false')
		const data = await res.json()
		console.log(data)
		coins = data;
	}
	loadCoins()
</script>

<h1>
	Hello World
</h1>
<table>
	<thead>
		<tr>
			<th> bla bla bla</th>
		</tr>
	</thead>
	<tbody>
	{#each coins as coin}
		<tr>
			<td>
				{coin.name}
			</td>
		</tr>
	{/each}

	</tbody>

</table>


<style>

</style>