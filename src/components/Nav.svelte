<script context="module">
</script>
<script>
  import {onMount,beforeUpdate,afterUpdate} from "svelte";
  export let currentPage;
  onMount(()=>{
    document.getElementById("myTopnav").className="topnav";
  })
  beforeUpdate(()=>{
    if(currentPage===undefined){
      currentPage="home";
    }
    document.querySelectorAll("a").forEach(a=>{
      a.style.background=""
    })
    document.getElementById(currentPage).style.background="#3880ff"
  });
  afterUpdate(()=>{
      if(currentPage===undefined){
        currentPage="home"
      }
      document.querySelectorAll("a").forEach(a=>{
        a.style.background=""
      })
      document.getElementById(currentPage).style.background="#3880ff";
      document.getElementById("toggle").removeAttribute("href");
  })
  function myFunction() {
    var x = document.getElementById("myTopnav");
    if (x.className === "topnav") {
      x.className += " responsive";
    } else {
      x.className = "topnav";
    }
  }
</script>
<style>
  @import "nav.css";
.topnav {
    overflow: hidden;
    background-color: #333;
}
      
.topnav a {
    float: left;
    display: block;
    color: #f2f2f2;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
    font-size: 17px;
}
      
.topnav a:hover {
    background-color: #ddd;
    color: black;
}
      
:global(.topnav a.active) {
    background-color: #3880ff;
    color: white;
}
      
.topnav .icon {
    display: none;
}
      
@media screen and (max-width: 600px) {
    .topnav a:not(:first-child) {display: none;}
        .topnav a.icon {
          float: right;
          display: block;
        }
    }
      
@media screen and (max-width: 600px) {
    :global(.topnav.responsive) {position: relative;}
        :global(.topnav.responsive .icon) {
          position: absolute;
          right: 0;
          top: 0;
        }
        :global(.topnav.responsive a) {
          float: none;
          display: block;
          text-align: left;
        }
    }
</style>

<div class="topnav" id="myTopnav">
    <a href="/#" id="home">Home</a>
    <a href="/about" id="about">About</a>
    <a href="/#" id="toggle" class="icon" on:click={myFunction}>
      <i class="fa fa-bars"></i>
    </a>
</div>