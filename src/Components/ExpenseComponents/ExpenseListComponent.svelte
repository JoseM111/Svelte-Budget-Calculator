<!-- ━━━━━━━━━ JS | TS ━━━━━━━━━ -->
<script>
	import {useStrict} from "../../main";
	import SectionTitle from "../TitleComponent.svelte";
	import Expense from "./ExpenseComponent.svelte";

	/**: - ©MEMBER-PROPERTIES| */
	/*| #™━━━━━━━━━━━━━━━━━━━━━|*/
	useStrict// JS STRICT
	// ━━━━━━━━━━━━━━━━━━━━━━━━
	export let expenses = []
	/*| #™━━━━━━━━━━━━━━━━━━━━━|*/

	/**| ™- LABELED-STATEMENT |*/
	/* #™━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ */

	/* #™━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ */

	/** #™━━━━━━━━━━━━━━━━━━━ FUNCTION ━━━━━━━━━━━━━━━━━━━ */
</script>
<!-- ⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️🔵🔵🔵🔵🔵🔵🔵🔵━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->

<div class="container">
	<!-- ━━━━━━━━━━━━━━━ CONTAINER ━━━━━━━━━━━━━━━ -->
	<!--⌛-->

	<!--⫷⫷⫷|@main|______________________________-->
	<section class="content">

		<!--⌨⌨⌨⌨|TITLE|⌨⌨⌨⌨-->
		<span class="expense-title">
		<SectionTitle title="expense list" />
		</span>
		<!--⌨⌨⌨⌨⌨⌨|END|⌨⌨⌨⌨⌨⌨-->

		<!--⌨⌨⌨⌨|ForEach On Expenses List|⌨⌨⌨⌨-->
		<ul>
			{#each expenses as expense}
				<!---->
				<!--<h4><i><b>Index: {i + 1} &nbsp;</b></i></h4>-->
				<!---->
				<Expense
					{...expense}
				/>
			{:else}
				<h2><b>Currently you have no expenses</b></h2>
			{/each}
		</ul>
		<!--⌨⌨⌨⌨⌨⌨|END|⌨⌨⌨⌨⌨⌨-->

	</section>
	<!--⫷⫷⫷|END|______________________________-->

	<!--⌛-->
	<!-- ━━━━━━━━━━━━━━━ CONTAINER ━━━━━━━━━━━━━━━ -->
</div>
<!-- ⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️🔵🔵🔵🔵🔵🔵🔵🔵━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->

<!-- ━━━━━━━━━ CSS | SCSS | SASS ━━━━━━━━━ -->
<style type="text/scss">
	@import 'src/styles/styles.scss';
	/* | ⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫ | */
	h1 {
		color: purple;
		font-size: 18px;
	}
	h2 {
		text-transform: capitalize;
		color: blue;
	}
	/* | ⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫ | */
	.expense-title {
		text-shadow: $txt-shadow3;
	}
	/* | ⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫ | */
</style>
<!-- ⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️🔵🔵🔵🔵🔵🔵🔵🔵━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
