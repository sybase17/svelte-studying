<script>
import { push } from "svelte-spa-router";


  
</script>

<head>
  <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
</head>
<header>

  <div class="header-logo">
    <p>YAMANAKA <br>APP</p>
  </div>

  <div class="menu-list">
    <ul>
      <li><a href="/"><span class="material-icons">home</span> HOME</a></li>
      <li><a on:click={()=>push('/add')} ><span class="material-icons">cloud</span> Coming Soon</a></li>
      <li><a on:click={()=>push('/add')} ><span class="material-icons">cloud</span> Coming Soon</a></li>
      <li><a on:click={()=>push('/add')} ><span class="material-icons">cloud</span> Coming Soon</a></li>
      <li><a on:click={()=>push('/add')} ><span class="material-icons">cloud</span> Coming Soon</a></li>
    </ul>
  </div>
  <span class="material-icons menu-icon">menu</span>

</header>


<style>
  header {
  background-color: #0bb582;
  width: 200px;
  height: 100%;
  position: fixed;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 80px 0px 40px;
  box-sizing: border-box;
}

.header-logo {
  text-align: center;
}


p{
  color: #ffffff;
  font-family: 'Courier New', Courier, monospace;
  font-size: 24px;
}


ul {
  list-style: none;
}

a {
  text-decoration: none;
}

.menu-list a {
  color: #ffffff;
  display: block;
  padding: 16px 24px;
  font-size: 18px;
}

.menu-list a:hover {
  background-color: #11ce66;
}
.material-icons{
  font-size: 15px;
}

.menu-icon{
  display: none;
}

</style>
