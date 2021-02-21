<!-- ━━━━━━━━━ JS | TS ━━━━━━━━━ -->
<script>
	import {useStrict} from "../../main"
	import {getContext} from "svelte";

	/**: - ©MEMBER-PROPERTIES| */
	/*| #™━━━━━━━━━━━━━━━━━━━━━|*/
	useStrict// JS STRICT
	// ━━━━━━━━━━━━━━━━━━━━━━━━
	export let id
	export let name = ''
	export let amount = 0
	export let displayAmount = false
	const removeExpense = getContext('remove')
	/*| #™━━━━━━━━━━━━━━━━━━━━━|*/

	/**| ™- LABELED-STATEMENT |*/
	/* #™━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ */

	/* #™━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ */

	/** #™━━━━━━━━━━━━━━━━━━━ FUNCTION ━━━━━━━━━━━━━━━━━━━ */

	const toggleAmt = () => {
		//___________
		console.log('Button clicked')
		displayAmount = !displayAmount
	}
	/// --> : toggleAmt ♠♠♠
</script>
<!-- ⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️🔵🔵🔵🔵🔵🔵🔵🔵━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->

<div class="container">
	<!-- ━━━━━━━━━━━━━━━ CONTAINER ━━━━━━━━━━━━━━━ -->
	<!--⌛-->

	<!--⫷⫷⫷|@main|______________________________-->
	<main>

		<!--⌨⌨⌨⌨|EXPENSE|⌨⌨⌨⌨-->
		<article class="single-expense">

			<!--⌨⌨⌨⌨|Expense-Info|⌨⌨⌨⌨-->
			<div class="expense-info">

				<!-- Button(Name)-->
				<h2>
					{name}
					<!--on:click|once={toggleAmt}-->
					<button
						class="amount-btn"
						on:click={toggleAmt}
					>
						<i class="fas fa-caret-down" />
					</button>
				</h2>
				<!-- Amount -->
				{#if displayAmount}<!-- #if -->
					<h4>
						<!---->
						<span class="amt">amount:</span>
						<!---->
						<span class="amt-txt">
					    ${amount}
				    </span>
					</h4>
				{/if}<!-- END: \if -->
			</div>
			<!--⌨⌨⌨⌨⌨⌨|END|⌨⌨⌨⌨⌨⌨-->

			<!--⌨⌨⌨⌨|Buttons|⌨⌨⌨⌨-->
			<div class="expense-buttons">
				<!-- Expense/Edit-Button -->
				<button class="expense-btn edit-btn">
					<i class="fas fa-pen"></i>
				</button>

				<!-- Delete-Button -->
				<button
					class="expense-btn delete-btn"
					on:click={removeExpense(id)}
				>
					<i class="fas fa-trash"></i>
				</button>
			</div>
			<!--⌨⌨⌨⌨⌨⌨|END|⌨⌨⌨⌨⌨⌨-->

		</article>
		<!--⌨⌨⌨⌨⌨⌨|END|⌨⌨⌨⌨⌨⌨-->

	</main>
	<!--⫷⫷⫷|END|______________________________-->

	<!--⌛-->
	<!-- ━━━━━━━━━━━━━━━ CONTAINER ━━━━━━━━━━━━━━━ -->
</div>
<!-- ⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️🔵🔵🔵🔵🔵🔵🔵🔵━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->

<!-- ━━━━━━━━━ CSS | SCSS | SASS ━━━━━━━━━ -->
<style type="text/scss">
	@import 'src/styles/styles.scss';
	/* | ⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫ | */
	.fa-pen {
		color: dodgerblue;
		text-shadow: $txt-shadow2;
	}
	.fa-trash {
		text-shadow: $txt-shadow2;
	}
	.fas {
		font-size: 28px;
		text-shadow: $txt-shadow2;
	}
	/* | ⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫ | */
	.amt {
		color: #afafaf;
		text-shadow: $txt-shadow2;
	}
	.amt-txt {
		color: orange;
		text-shadow: $txt-shadow2;
	}
	/* | ⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫ | */
	button {
		outline: none;
		font-size: 22px;
	}
	button:active {
		opacity: 0.45;
	}
	//button, .amount-btn {
	//	// ... existing styles
	//	transition: 280ms all 120ms ease-out;
	//}
	/* | ⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫ | */
	h2 {
		color: black;
		font-weight: $semi-bold;
		text-shadow: $txt-shadow2;
	}
	/* | ⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫ | */
</style>
<!-- ⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️🔵🔵🔵🔵🔵🔵🔵🔵━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
