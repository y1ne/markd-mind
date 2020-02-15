<template>
    <div class="container">
	<header class="header">header</header>
	<main   class="main"  >
	    <div class="hello">
		<h1>{{ msg }}</h1>
	    </div>
	</main>
	<aside  class="aside" >aside</aside>
	<nav    class="nav"   >nav</nav>
	<footer class="footer">footer</footer>
    </div>
</template>

<script>
export default {
  name: 'Index',
  data () {
    return {
      msg: 'Welcome to markd-mind'
    }
  }
}
</script>


<style>
 .container {
     border: solid 1px black;
     display: grid;
     /* 1列目から順番に180px、1fr、160pxの幅 */
     grid-template-columns: 180px 1fr 160px;
     /* 1行目から順番に60px 1fr 90pxの高さ */
     grid-template-rows: 60px 1fr 600px;
 }
 .header {
     border: solid 1px black;

     /* 列の1本目から4本目のグリッドラインまで */
     grid-column-start: 1;
     grid-column-end: 4;
     /* 行の1本目から2本目のグリッドラインまで */
     grid-row-start: 1;
     grid-row-end: auto;
 }

 .main {
     border: solid 1px black;
     /* 列の2本目から3本目のグリッドラインまで */
     grid-column-start: 2;
     grid-column-end: auto;
     /* 行の2本目から3本目のグリッドラインまで */
     grid-row-start: 2;
     grid-row-end: 4;
 }

 .aside {
     border: solid 1px black;
     /* 列の1本目から2本目のグリッドラインまで */
     grid-column-start: 1;
     grid-column-end: auto;
     /* 行の2本目から3本目のグリッドラインまで */
     grid-row-start: 2;
     grid-row-end: auto;
 }

 .nav {
     border: solid 1px black;
     /* 列の3本目から4本目のグリッドラインまで */
     grid-column-start: 3;
     grid-column-end: auto;
     /* 行の2本目から3本目のグリッドラインまで */
     grid-row-start: auto;
     grid-row-end: auto;
 }

 .footer {
     border: solid 1px black;
     /* 列の1本目から4本目のグリッドラインまで */
     grid-column-start: 1;
     grid-column-end: 4;
     /* 行の3本目から4本目のグリッドラインまで */
     grid-row-start: auto;
     grid-row-end: auto;
 } 
</style>
