<!-- ━━━━━━━━━ JS | TS ━━━━━━━━━ -->
<script>
	import NavBarComponent from '../Components/NavBarComponent.svelte'
	import expensesData from '../mock-data/expenses'
	import ExpenseListComponent from "../Components/ExpenseComponents/ExpenseListComponent.svelte"
	import {useStrict} from "../main"
	import {setContext} from "svelte";

	/**: - ©MEMBER-PROPERTIES| */
	/*| #™━━━━━━━━━━━━━━━━━━━━━|*/
	useStrict
	let expenses = [...expensesData]
	/*| #™━━━━━━━━━━━━━━━━━━━━━|*/

	/**| ™- LABELED-STATEMENT |*/
	/* #™━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ */
	$: console.log(expenses)
	/* #™━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ */

	/** #™━━━━━━━━━━━━━━━━━━━ FUNCTION ━━━━━━━━━━━━━━━━━━━ */

	const removeExpense = (id) => {
		//___________
		expenses = expenses
			.filter(item => item.id !== id)
	}
	/// --> : removeExpense ♠♠♠

	setContext('remove', removeExpense)
	/// --> : setContext ♠♠♠

</script>
<!-- ⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️🔵🔵🔵🔵🔵🔵🔵🔵━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->

<div class="container">
	<!-- ━━━━━━━━━━━━━━━ CONTAINER ━━━━━━━━━━━━━━━ -->
	<!--⌛-->

		<!--⌨⌨⌨⌨|Nav-Bar|⌨⌨⌨⌨-->
		<NavBarComponent/>
		<!--⌨⌨⌨⌨⌨⌨|END|⌨⌨⌨⌨⌨⌨-->

	<!--⫷⫷⫷|@main|______________________________-->
	<main>


		<ExpenseListComponent {expenses} />


	</main>
	<!--⫷⫷⫷|END|______________________________-->

	<!--⌛-->
	<!-- ━━━━━━━━━━━━━━━ CONTAINER ━━━━━━━━━━━━━━━ -->
</div>
<!-- ⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️🔵🔵🔵🔵🔵🔵🔵🔵━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->

<!-- ━━━━━━━━━ CSS | SCSS | SASS ━━━━━━━━━ -->
<style type="text/scss">
	@import '../styles/styles';
	/* | ⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫ | */
	b {
		font-size: 25px;
	}
	/* | ⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫ | */
	/* | ⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫⌫ | */
</style>
<!-- ⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️⚫️🔵🔵🔵🔵🔵🔵🔵🔵━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->

