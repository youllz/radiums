<section id="footer">
	<div class="footer-top">
		<p class="logo">
			{#each 'RADIUMS' as letter}
				<span>
					{letter}
				</span>
			{/each}
		</p>
	</div>
	<div class="footer-mid">
		<div class="mid-left">
			<ul>
				<li>
					<a href="/">
						<svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-width="4"><path stroke-dasharray="24" stroke-dashoffset="24" d="M17 4L15 4C12.5 4 11 5.5 11 8V20"><animate fill="freeze" attributeName="stroke-dashoffset" dur="0.4s" values="24;0"/></path><path stroke-dasharray="12" stroke-dashoffset="12" d="M8 12H15"><animate fill="freeze" attributeName="stroke-dashoffset" begin="0.5s" dur="0.2s" values="12;0"/></path></g></svg>
					</a>
				</li>
				<li>
					<a href="/">
						<svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24"><circle cx="4" cy="4" r="2" fill="currentColor" fill-opacity="0"><animate fill="freeze" attributeName="fill-opacity" dur="0.4s" values="0;1"/></circle><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-width="4"><path stroke-dasharray="12" stroke-dashoffset="12" d="M4 10V20"><animate fill="freeze" attributeName="stroke-dashoffset" begin="0.2s" dur="0.2s" values="12;0"/></path><path stroke-dasharray="12" stroke-dashoffset="12" d="M10 10V20"><animate fill="freeze" attributeName="stroke-dashoffset" begin="0.5s" dur="0.2s" values="12;0"/></path><path stroke-dasharray="24" stroke-dashoffset="24" d="M10 15C10 12.2386 12.2386 10 15 10C17.7614 10 20 12.2386 20 15V20"><animate fill="freeze" attributeName="stroke-dashoffset" begin="0.7s" dur="0.5s" values="24;0"/></path></g></svg>
					</a>
				</li>
				<li>
					<a href="/">
						<svg xmlns="http://www.w3.org/2000/svg" width="22" height="22" viewBox="0 0 24 24"><g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"><path stroke-dasharray="66" stroke-dashoffset="66" d="M12 3H8C5.23858 3 3 5.23858 3 8V16C3 18.7614 5.23858 21 8 21H16C18.7614 21 21 18.7614 21 16V8C21 5.23858 18.7614 3 16 3z"><animate fill="freeze" attributeName="stroke-dashoffset" dur="0.6s" values="66;132"/></path><path stroke-dasharray="26" stroke-dashoffset="26" d="M12 8C14.20914 8 16 9.79086 16 12C16 14.20914 14.20914 16 12 16C9.79086 16 8 14.2091 8 12C8 9.79086 9.79086 8 12 8"><animate fill="freeze" attributeName="stroke-dashoffset" begin="0.7s" dur="0.4s" values="26;0"/></path></g><circle cx="17" cy="7" r="1.5" fill="currentColor" fill-opacity="0"><animate fill="freeze" attributeName="fill-opacity" begin="1.1s" dur="0.4s" values="0;1"/></circle></svg>
					</a>
				</li>
			</ul>
			<div>
				<a href="mailto:zyoussouf70@gmail.com">radiumsagency@gmail.com</a>
			</div>
		</div>
		<a href="/">
			Retourner en haut
		</a>
	</div>
</section>



<style>

	section {
		padding: 8vw 5vw 2vw 5vw;
		display: grid;
		gap: 40px;
	}
	.footer-top {
		width: 100%;
	}

	.logo {
		font-size: clamp(30px, 10vw + 0.1rem, 15rem);
		text-align: center;
	}

	.footer-mid {
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: space-between;
		gap: 20px;
	}

	.mid-left {
		display: flex;
		align-items: center;
		gap: 20px;

		
	}


	.mid-left ul {
		display: flex;
		align-items: center;
		gap: 20px;
	}

	@media (width < 500px) {
		.mid-left {
			flex-direction: column;
		}
		.footer-mid {
			flex-direction: column;
		}
	}
</style>