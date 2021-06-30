<script>
  export let holiday;
  let picNum = 1;
  let newPicNum = picNum += 1;
  let src=""
</script>


<article class="holiday">
  <h1>{holiday.name}</h1>
  <small>
    Date: <b>{holiday.date}</b>
  </small><br/>
  <img src="https://source.unsplash.com/random/100x100?sig=1" alt="randomness"><br/>
  <!-- <img src="https://picsum.photos/id/{newPicNum}" alt="brokenLink"/> -->
  <small>
    This year it falls on a <b>{holiday.weekday.date.name}</b>
  </small>
</article>

<style>
  article {
    display: grid;
    grid-template-columns: 1fr;
    margin: 0 0 1em 0;
    border: 1px solid orange;
    padding: 10px;
    height: 222px;
    box-shadow: 0 30px 50px 0 rgb(49 49 55 / 10%);
    background-color: #fff;
    border-radius: 20px;
    box-shadow: 0 10px 40px rgb(0 0 0 / 20%);
  }

  h1 {
    /* font-size: 1.4em; */
    margin: 0;
    display: block;
    color: #ff3e00;
		text-transform: uppercase;
		font-size: 1em;
		font-weight: 400;
    text-align: center;
  }
  img{
    margin: auto;
  }
</style>
