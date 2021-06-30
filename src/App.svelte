<script>
	import { onMount } from 'svelte';
  import Holiday from './Holiday.svelte';
  import Holidays from './Holidays.svelte';
  import Employees from './Employees.svelte';
  import Directory from './Directory.svelte';

  let holidays;
  let holiday;

</script>


<main>
  <Directory />
  <h1>Holidays this month</h1>
  <Holidays {holidays} />
  <Employees />
</main>

<style>

	main {
    display: grid;
    grid-template-columns: 300px 300px 300px;
		text-align: center;
		margin: 0 auto;
    gap: 5px;
	}


	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 3em;
		font-weight: 300;
    text-align: center;
    grid-column-start: 1;
    grid-column-end: 4;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
