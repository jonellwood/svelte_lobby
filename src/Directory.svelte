<script>
import Icon from 'fa-svelte'
import { faCircle } from '@fortawesome/free-solid-svg-icons/faCircle'
let icon = faCircle;
</script>


<div class="wrapper">


  <div class="directory">
    <div id="singleDirectory"> <Icon class="icon" icon={icon}></Icon> Police Dispatch  <br> 1st Floor</div>
    <div id="singleDirectory"> <Icon class="icon" icon={icon}></Icon> Courtroom <br> 1st Floor</div>
    <div id="singleDirectory"> <Icon class="icon" icon={icon}></Icon> Courtroom <br> 1st Floor</div>
    <div id="singleDirectory"> <Icon class="icon" icon={icon}></Icon> Clerk of Court <br> 1st Floor</div>
    <div id="singleDirectory"> <Icon class="icon" icon={icon}></Icon> Building & Codes <br> 1st Floor</div>
    <div id="singleDirectory"> <Icon class="icon" icon={icon}></Icon> Public Restrooms <br> 1st Floor</div>
    <div id="singleDirectory"> <Icon class="icon" icon={icon}></Icon> Police Records <br> 2nd Floor</div>
    <div id="singleDirectory"> <Icon class="icon" icon={icon}></Icon> City Admin Offices <br> 2nd Floor</div>
    <div id="singleDirectory"> <Icon class="icon" icon={icon}></Icon> Emily Huff <br> 2nd Floor</div>
  </div>
</div>

<style>
  .wrapper{
    position: absolute;
    right:0;
    z-index: 2;
    margin-right: 30em;
    margin-top: 5px;
  }
  /* .icon{
    color: hotpink;
  } */
  .directory{
    display: grid;
    grid-template-columns: 1fr;
    gap: 5px;

  }
  #singleDirectory{
    border: 1px solid orange;
    display: grid;
    grid-template-columns: .25fr 1fr;
    /* width:fit-content; */
    border: 1px solid orange;
    padding: 10px;
    box-shadow: 0 30px 50px 0 rgb(49 49 55 / 10%);
    background-color: #fff;
    border-radius: 20px;
    box-shadow: 0 10px 40px rgb(0 0 0 / 20%);
  }
</style>
