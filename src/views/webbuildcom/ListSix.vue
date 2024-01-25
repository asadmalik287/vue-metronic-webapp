<!-- HeaderComponent.vue -->

<template>
<div class="table-responsive">
	<table class="table table-rounded table-row-bordered border gy-7 gs-7">
		<thead>
			<tr class="fw-semibold fs-6 text-gray-800 border-bottom-2 border-gray-200">
				<th>Name</th>
				<th>Position</th>
				<th>Office</th>
				<th>Age</th>
				<th>Start date</th>
				<th>Salary</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>Tiger Nixon</td>
				<td>System Architect</td>
				<td>Edinburgh</td>
				<td>61</td>
				<td>2011/04/25</td>
				<td>$320,800</td>
			</tr>
			<tr class="table-active">
				<td>Garrett Winters</td>
				<td>Accountant</td>
				<td>Tokyo</td>
				<td>63</td>
				<td>2011/07/25</td>
				<td>$170,750</td>
			</tr>
		</tbody>
	</table>
</div>
</template>

<script>
export default {
  htmlCode: `<div class="table-responsive">
	<table class="table table-rounded table-row-bordered border gy-7 gs-7">
		<thead>
			<tr class="fw-semibold fs-6 text-gray-800 border-bottom-2 border-gray-200">
				<th>Name</th>
				<th>Position</th>
				<th>Office</th>
				<th>Age</th>
				<th>Start date</th>
				<th>Salary</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>Tiger Nixon</td>
				<td>System Architect</td>
				<td>Edinburgh</td>
				<td>61</td>
				<td>2011/04/25</td>
				<td>$320,800</td>
			</tr>
			<tr class="table-active">
				<td>Garrett Winters</td>
				<td>Accountant</td>
				<td>Tokyo</td>
				<td>63</td>
				<td>2011/07/25</td>
				<td>$170,750</td>
			</tr>
		</tbody>
	</table>
</div>`,
};
</script>

<style scoped>
/* Add any component-specific styles here */
</style>
