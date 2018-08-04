
<!DOCTYPE HTML>
<html lang="en-GB">
<head>
<title> John_Betong's Application Switcher </title>
<meta name=viewport content="width=device-width, initial-scale=1">

<style> 
/* 
  WRITEPATH css/style_spirals.css
  SitePoint: Paul O'Brien 
*/
html {
  box-sizing: border-box;
}
*,
*:before,
*:after {
  box-sizing: inherit;
}
body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
}
.col h3 {margin: 0;}
.circle {
  position: relative;
  margin: 0;
  width: 125px; height: 125px;
  border: 15px solid transparent; border-radius: 50%;
}
.circle1 {
  border-color: #29bdcc;
  border-left-color: transparent;
  border-top-color: transparent;
}
.circle2 {border-color: #17556f; border-right-color: transparent;}
.circle3 {border-color: #f58c31; border-left-color:  transparent;}
.circle4 {border-color: #ed4565; border-right-color: transparent;}
.circle5 {border-color: #f0b224; border-left-color:  transparent;}
.circle6 {border-color: #1eb473; border-right-color: transparent;}
.circle7 {border-color: #93288d; border-left-color:  transparent;}
.circle8 {border-color: #1b5f8c; border-right-color: transparent;}
.circle h2 {display: table; margin: 5px 0 0 5px;
  width: 85px; height: 85px;
  background: #29bdcc; border-radius: 50%;
}
.circle2 h2 {background: #17556f;}
.circle3 h2 {background: #f58c31;}
.circle4 h2 {background: #ed4565;}
.circle5 h2 {background: #f0b224;}
.circle6 h2 {background: #1eb473;}
.circle7 h2 {background: #93288d;}
.circle8 h2 {background: #1b5f8c;}
.circle span {font-size: 12px;
  color: #fff; display: table-cell;
  vertical-align: middle;text-align: center;}
.circle i,
.circle b {font-weight: bold; font-style: normal; display: block;}
.circle i {font-size: 24px;}
.wrap { display: flex; flex-wrap: wrap; max-width: 980px; margin: auto;}
.col {
  flex: 1 0 50%;
  display: flex;
  align-items: center;
  margin-bottom: -47px;
  position: relative;
  left: 23px;
}
.col2 {left: -24px;}
.col1 {text-align: right; align-content: flex-end;}
.col1 .content {order: -1;}
.content {flex: 1 0 0%; padding: 1px 10px; margin:-20px 0;}
.content h2 {font-size: 1 rem;}
.content p {margin: 0.5em 0 0 0; font-size: 0.8rem; color: #666;}
.circle1:before {
  content: "";
  height: 15px; width: 250px;
  position: absolute; right: 46px; top: -15px;
  background: #29bdcc;
  background:linear-gradient(to left, #29bdcc 0%, white 100%);
  z-index: -1; animation:shimmer 10s infinite forwards;}
@keyframes shimmer{
  0%  {width: 0;}
  5%  {width: 250px;}
  100%{width: 250px;}
}
.circle1:after,
.circle8:after {
  content: "";
  position: absolute;
  left: -15px;
  top: -15px;
  width: 125px; height: 125px;
  border: 15px solid transparent;
  border-color: #29bdcc;
  border-left-color: transparent;
  border-top-color: transparent;
  transform: rotate(-45deg);
  border-radius: 50%;
  z-index: -1;
}
.circle8:after {
  border-color: #1b5f8c;
  border-right-color: transparent;
  border-bottom-color: transparent;
  transform: rotate(-45deg);
}
.circle8:before {
  content: "";
  height: 15px;
  width: 250px;
  position: absolute;
  right: -202px;
  bottom: -15px;
  background: #1b5f8c;
  background:linear-gradient(to right, #1b5f8c 0%, white 100%);
  z-index: -1;
}
.circle8 {border-bottom-color: transparent;}
@media screen and (max-width: 600px) {
  .wrap {
    display: block;
  }
  .content{margin:0;}
  .col {
    margin: 10px 0;
    position: static;
  }
  .circle8:before,
  .circle8:after,
  .circle1:before,
  .circle2:after {
    display: none;
  }
  .circle1 {border-color: #29bdcc;}
  .circle2 {border-color: #17556f;}
  .circle3 {border-color: #f58c31;}
  .circle4 {border-color: #ed4565;}
  .circle5 {border-color: #f0b224;}
  .circle6 {border-color: #1eb473;}
  .circle7 {border-color: #93288d;}
  .circle8 {border-color: #1b5f8c;}
}


/* ====== MENU DROPDOWN  ========== */
.dropdown {
  position: relative;
  display: inline-block;
  background-color: #dff;
  padding: 0.12em .42em;
}
.dropdown-content {
  display: none;
  position: absolute;
  background-color: #f9f9f9;
  min-width: 14em;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  padding: 12px 42px 12px 4px;
  line-height: 2em;
  z-index: 1;
  background-color:#eee;
}
.dropdown:hover .dropdown-content {
  display: block;
  width: 8em;
}
.dropdown-content a:hover {
  background-color: #00f; color: #fff;
}

.ftr {position:fixed; bottom: 0; left: 0; width: 100%;}.home {position:fixed; top:4px; left:4px; margin:0; padding:0;}

.bge  {background-color:#eee; color:#000;}
.ftr  {position:fixed; bottom: 0; left:0; width:100%;}
/*
  ftr tac bge lh2 hg2
*/
.fll  {float: left;}.flr  {float: right;} 
.hg2  {height:2em;}
.lh2  {line-height:2em;}
.ooo  {margin:0; padding:0;} 
.tac  {text-align:center;}
a       {
  border:outset 1px transparent; 
  padding: 0.42em 0.88em;
}
a:hover {
  background-color: #9ff; color: #000; 
  border: outset 1px #00a;
}
div {outline:solid 0px red;}
</style>
</head>
<body>

  <h1 class="clb tac"> CodeIgniter4-Dev's Application Folder </h1>
  <h4 class="tac ooo"> Validation Modifications </h4>

  <div> 
    no errors! 
    <b class="flr"> production </b>
  </div>
  
  <hr>
  <p> <br> </p>

<div class="wrap">

  <div class="col col1"></div>
  <div class="col col2">
    <div class="circle circle1">
      <h2><span><b>  </b> <i> Done </i></span></h2>
    </div>
    <div class="content">
      <h3> <a href="https://johns-jokes.cf/v_blurb?app=7"> Blurb  &#10004; </a> </h3>
      <p>  AmpProject, Top Menu, SVG Diagaonal, Footer, Views </p>
    </div>
  </div>

  <div class="col col1">
    <div class="circle circle2">
      <h2><span><b></b> <i>Done</i></span></h2>
    </div>
    <div class="content">
      <h3> <a href="https://johns-jokes.cf/welcome?app=7"> Original welcome-message  &#10004;</a> </h3>
      <p>  Blogs, Links to every blog </p>
    </div>
  </div>
  <div class="col col2"></div>
  <div class="col col1"></div>

  <div class="col col2">
    <div class="circle circle3">
      <h2><span><b></b> <i>ToDo</i></span></h2>
    </div>
    <div class="content">
      <h3> <a href="https://johns-jokes.cf/v_welcome_message?app=7"> Valid welcome_message &#x2714;</a> </h3>
      <p>  Pagination! Display each novel with links to pages. </p>
    </div>
  </div>

  <div class="col col1">
    <div class="circle circle4">
      <h2><span><b></b> <i>Done</i></span></h2>
    </div>
    <div class="content">
      <h3> <a href="https://johns-jokes.cf/v_mods?app-7">  Modification Details &#10004;</a> </h3>
      <p>  Validate Uploads to server. Check Error Log </p>
    </div>
  </div>
  <div class="col col2"></div>
  <div class="col col1"></div>
  
  <div class="col col2">
    <div class="circle circle5">
      <h2><span><b></b> <i>ToDo</i></span></h2>
    </div>
    <div class="content">
      <h3> <a href="https://johns-jokes.cf/v_github?app=7 "> GitHub Update Changes </a> </h3>
      <p>  Validate Uploads to server. Check Error Log </p>
    </div>
  </div>
  
  <div class="col col1">
    <div class="circle circle6">
      <h2><span><b></b> <i>ToDo</i></span></h2>
    </div>
    <div class="content">
      <h3> Google Stuff </h3>
      <p>  Analytics, Analysis, Adsense </p>
    </div>
  </div>
  <div class="col col2"></div>
  <div class="col col1"></div>

  <div class="col col2">
    <div class="circle circle7">
      <h2><span><b></b> <i>ToDo</i></span></h2>
    </div>
    <div class="content">
      <h3> Optimisation </h3>
      <p>  Especially images. Also Cache PHP files to HTML and modify htaccess to bypass PHP and MySql </p>
    </div>
  </div>
  
  <div class="col col1">
    <div class="circle circle8">
      <h2><span><b></b> <i>ToDo</i></span></h2>
    </div>
    <div class="content">
      <h3> Promotion </h3>
      <p>  Let everyone know including the cat, dog and canary! </p>
    </div>
  </div>
  <div class="col col2"></div>
</div><!-- class="wrap" -->
<p>
  <br><br><br><br>
</p>


<div class="ftr tac bge lh2 hg2">
  Wonderful place for a footer
</div>

</body>
</html>
