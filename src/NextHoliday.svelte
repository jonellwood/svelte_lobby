<script>
  import { onMount } from 'svelte';

  export let holidays = [];
  export let holiday;

  onMount(async () => {
    await fetch (`https://holidayapi.com/v1/holidays?pretty&key=edb48c75-31ef-4c37-94ea-e30a98d9ceeb&country=US&year=2021&month=7&day=6&upcoming=true`)
    .then(r => r.json())
    .then(data => {
      holidays = data;
    });
    console.log(holidays.holidays[0].name);
  } )
</script>

{#if holidays.holidays}
  <div>
    <h1>Upcoming Holiday</h1>
    <p class="singleHoliday">

      On {holidays.holidays[0].date} it will be {holidays.holidays[0].name}
    </p>

  </div>
    {/if}

<style>
  div{

    border: 1px darkorange solid;
    border-radius: 7px;
    box-shadow: 5px 5px 5px 10px lightgray;
  }
  p{
    font-size: xx-large;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    margin-left: 10px;
    margin-right: 10px;
  }
  h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 2.5em;
		font-weight: 300;
    text-align: center;
</style>
