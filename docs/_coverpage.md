<!-- _coverpage.md -->
<!-- # HyUI <small>4.0</small> -->

<div class="info">

<h1>
<span class="title"><img src="vue_LOGO.png"  style="max-width:300px;"></span>
<span class="admin">Admin Dashboard</span>
</h1>

<div class="subtitle">
<p>透過 Vuetify3 文件搭建的ＵＩ模版，快速搭建後台頁面</p>
</div>

<div class="btnList">
<span >
  <a href="#?id=hyvue-cms">Get Started</a>
</span>
<span >
  <a class="github" href="https://github.com/HywebU00/HyVue_CMS">GitHub</a>
</span>
</div>
</div>

<style>
  .logo{
    width: 360px;
    margin: 0 auto;
    position: relative;
  }
  .logo span{
    margin-right: 2em;
    text-align: end;
    position: absolute;
    top: 1.25em;
    color:#336699;
    right: 0;
  }
  
  section.cover a{
    border-radius: 0.5rem;
    color:#fff;
    display: inline-block;
    font-size: 1.05rem;
    letter-spacing: .1rem;
    margin: 0.5rem 1rem;
    padding: 0.75em 2rem;
    text-decoration: none;
    transition: all .15s ease;
    width:180px;
    margin: 0.25em;
    background: rgb(0,93,157); /* Old browsers */
    

background-size: 300% 100%;
}
section.cover a:hover{
background-position: 100% 0;
moz-transition: all .4s ease-in-out;
-o-transition: all .4s ease-in-out;
-webkit-transition: all .4s ease-in-out;
transition: all .4s ease-in-out;
background: #044d7f;
}
section.cover a.github{
border:1px solid #336699 !important;
background:unset;
color:#336699;
transition: all .4s ease-in-out;


}
section.cover a.github:hover{
  background:#e7fff8;
}

.subtitle{
  margin-top:2rem;
 
}

.cover.show{
background:#fff !important;
}
@media screen and (max-width: 1440px){
.cover.show{
background-size:40% !important;
}
}
@media screen and (max-width: 1200px){
.cover.show{
background-size:50% !important;
}
}
@media screen and (max-width: 767px){
.cover.show{
background-image:none !important;
}
.cover.show:after{
background-position: center;
}
.info{
margin: 0 0 10% 0;
}
}
.cover.show:after{
content:'';
background-image: url(cover_bg.png) !important;

width: 100%;
position: absolute;
height: 100%;
z-index: -1;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: right;

}
section.cover h1{
color:#165fa7;
font-size: 3rem;
font-weight: 700;
margin:0.75em 0 0 0;

}
section.cover h1 .admin{
margin-top:-0.5rem;
display: block;
font-weight: 500;
font-size: 2.3rem;
letter-spacing: -0.1rem;
}
section.cover p {
/* color:#165fa7; */
font-size: 1.2em;
margin-top: 0em;
margin-bottom:1.75em;
}
</style>
