<template>
  <div>
    <nav>
    <ul>
      <li>Home</li>
      <li>About</li>
      <li>Products</li>
      <li>Services</li>
      <li>Blog</li>
      <li>Contact</li>
    </ul>
     <div class="icons">
					<img class="icon-1" src="img/icon-1.png">
					<img class="icon-2" src="img/icon-2.png">
            </div>
    </nav>
  </div>
</template>

<script>
export default {

  }
</script>
<style>
nav {
  width: 100%;
  height: 80px;
  padding: 25px;
  background: #383b37;
  color: #fff;
  box-shadow: 0px 5px 10px rgba(0, 0, 0, 0.2);
  display: flex;
  justify-content: center;
  align-items: center;
  font-weight: bold;
  font-size: 16px;
  line-height: 23px;
}

ul,
li {
  list-style-type: none;
}
a {
  text-decoration: none;
}

a,
a:visited,
a:active {
  color: #fff;
}

nav ul {
  display: flex;
  margin-right: 25px;
}

nav ul li {
  cursor: pointer;
  padding: 0 40px;
  font-size: 16px;
}

nav ul li:not(:last-child) {
  border-right: 1px solid black;
}


nav .icons {
  display: flex;
}

nav .icons .icon-1{
  height: 30px;
  margin: 0px 20px;
}


nav .icons .icon-2{
  height: 30px;
  margin: 0px 20px;
  
}

</style>