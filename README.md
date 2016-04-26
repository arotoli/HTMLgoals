# HTMLgoals
currently my project at musicproductionempire.com is underway. This experiment has been born to accelerate my skills in web design and development




<!DOCTYPE html>
<html lang="en">
<head>

    <script>
    $('#navcontainer').slicknav({
		prependTo:'#demo1'
});
 
    </script>
    
    <script>
	$(function(){
		$('#navcontainer').slicknav();
	});
</script>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.2.0/jquery.min.js"></script>

    
    <script>jQuery(document).ready(function ($) {

  $('#checkbox').change(function(){
    setInterval(function () {
        moveRight();
    }, 300);
  });
  
	var slideCount = $('#slider ul li').length;
	var slideWidth = $('#slider ul li').width();
	var slideHeight = $('#slider ul li').height();
	var sliderUlWidth = slideCount * slideWidth;
	
	$('#slider').css({ width: slideWidth, height: slideHeight });
	
	$('#slider ul').css({ width: sliderUlWidth, marginLeft: - slideWidth });
	
    $('#slider ul li:last-child').prependTo('#slider ul');

    function moveLeft() {
        $('#slider ul').animate({
            left: + slideWidth
        }, 500, function () {
            $('#slider ul li:last-child').prependTo('#slider ul');
            $('#slider ul').css('left', '');
        });
    };

    function moveRight() {
        $('#slider ul').animate({
            left: - slideWidth
        }, 500, function () {
            $('#slider ul li:first-child').appendTo('#slider ul');
            $('#slider ul').css('left', '');
        });
    };

    $('a.control_prev').click(function () {
        moveLeft();
    });

    $('a.control_next').click(function () {
        moveRight();
    });

});    
        
        
</script>
    
    <script>
var x = document.getElementById("demo");

function getLocation() {
    if (navigator.geolocation) {
        navigator.geolocation.getCurrentPosition(showPosition, showError);
    } else {
        x.innerHTML = "Geolocation is not supported by this browser.";
    }
}

function showPosition(position) {
    var latlon = position.coords.latitude + "," + position.coords.longitude;

    var img_url = "http://maps.googleapis.com/maps/api/staticmap?center="
    +latlon+"&zoom=14&size=400x300&sensor=false";
    document.getElementById("mapholder").innerHTML = "<img src='"+img_url+"'>";
}

function showError(error) {
    switch(error.code) {
        case error.PERMISSION_DENIED:
            x.innerHTML = "User denied the request for Geolocation."
            break;
        case error.POSITION_UNAVAILABLE:
            x.innerHTML = "Location information is unavailable."
            break;
        case error.TIMEOUT:
            x.innerHTML = "The request to get user location timed out."
            break;
        case error.UNKNOWN_ERROR:
            x.innerHTML = "An unknown error occurred."
            break;
    }
}
</script>
    
    
  <!-- Basic Page Needs
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <meta charset="utf-8">
  <title>MPE</title>
  <meta name="description" content="">
  <meta name="author" content="SecondPHP">

  <!-- Mobile Specific Metas
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <!-- FONT
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <link href="http://fonts.googleapis.com/css?family=Raleway:400,300,600" rel="stylesheet" type="text/css">

  <!-- CSS
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <link rel="stylesheet" href="normalize.css">
  <link rel="stylesheet" href="skeleton.css">
     <link rel="stylesheet" href="php15.css">
    <link rel="stylesheet" href="SlickNav/slicknav.css" />
<link rel="icon" type="image/ico" href="http://localhost:8888/introphp/favicon.ico"/>
    <link rel="stylesheet" type="text/css" href="slideOut.css">
    <link href='https://fonts.googleapis.com/css?family=Rock+Salt' rel='stylesheet' type='text/css'>
        

  <style>


      .slicknav_navcontainer {
	display:none;
}

@media screen and (max-width: 480px) {
	/* #menu is the original menu */
	.js #navcontainer {
		display:none;
	}
	
	.js .slicknav_menu {
		display:block;
	}
}
    /*  #circle {
  position: relative;
  background-color: #09f;
  margin: 20px auto;
  width: 400px;
  height: 600px;
  border-radius: 200px;
}
      */
      
      
      @media screen and (max-width: 480px){
      header{
      font-size: 2em;
      }}
      
            @media screen and (max-width: 320px){
      header{
      font-size: 1em;
      }}
#text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #fff;
}
      
      body{
    margin:0;
          background-image: url(background.jpg);
}

      #cp_widget_24b1289d-2e8d-449f-83e3-1dc0245ba117{
          margin-left: 40%;
      }
#box1{
    width: 100%;
    height:150px;
    position:relative;
    margin-top: -100px;
    margin-bottom: -20px;
}

#theX{
    width:200px;
    height:0px;
}
.slidingOut{
     transition: left 1s;
     left:0px;
     background-color:white;
}
.slidingIn{
     transition: left 1s;
     left:-85%;
     background-color:white;
}
      
      
      #menuouter{
       display: table;   /* Allow the centering to work */
	margin: 0 auto;   
      }
      div#navcontainer
{
position: relative;
font: small-caps bold small/24px "Times New Roman", serif;
letter-spacing: 1px;
text-align: center;
}

ul#navlist
{
border-top: 1px solid #fff;
margin: 0;
width: 480px;
/* 4 * 120px li */
}

ul#subnavlist
{
border-bottom: 2px solid #444;
border-left: 1px solid #444;
border-right: 1px solid #888;
margin: 0;
padding: 0;
position: absolute;
top: 30px;
width: 120px;
}

/* all buttons */
ul#navlist li > a:link, ul#navlist li > a:visited, ul#navlist li * a:link, ul#navlist li * a:visited
{
text-decoration: none;
width: 120px;
}

#navlist li
{
display: inline;
list-style-type: none;
margin: 0;
padding: 0;
}

/* parents */
ul#navlist li > a:link, ul#navlist li > a:visited
{
background: #F60;
border-bottom: 5px solid #ccc;
border-top: 0;
color: #c00;
float: left;
}

ul#navlist li > a:hover
{
background: #f5f5f5;
border-bottom: 4px solid #eee;
border-top: 1px solid #fff;
color: #000;
}

/* children */
ul#navlist li * a:link, ul#navlist li * a:visited
{
background: #ccc;
border-bottom: 0;
border-top: 2px solid #bbb;
color: #777;
display: block;
float: none;
}

ul#navlist li * a:hover
{
background: #999;
border-bottom: 1px solid #888;
border-top: 1px solid #eee;
color: #fff;
}

/* active states */
a:link[id=current], a:visited[id=current]
{
background: #c30 !important;
color: #000 !important;
}

a:hover[id=current] { background: #f5f5f5 !important; }

a:link[id=subcurrent], a:visited[id=subcurrent]
{
background: #444 !important;
color: #fff !important;
}

a:hover[id=subcurrent] { background: #000 !important; }
      
      @media screen and (max-width: 480px){
          
          
      
      }
      header{
              font-family: 'Rock Salt', cursive;
      }
      
      @import url(http://fonts.googleapis.com/css?family=Open+Sans:400,300,600);	

html {
  border-top: 5px solid #fff;
  background: #58DDAF;
  color: #2a2a2a;
}

html, body {
  margin: 0;
  padding: 0;
  font-family: 'Open Sans';
}

h1 {
  color: #fff;
  text-align: center;
  font-weight: 300;
}

#slider {
  position: relative;
  overflow: hidden;
  margin: 20px auto 0 auto;
  border-radius: 4px;
}

#slider ul {
  position: relative;
  margin: 0;
  padding: 0;
  height: 200px;
  list-style: none;
}

#slider ul li {
  position: relative;
  display: block;
  float: left;
  margin: 0;
  padding: 0;
  width: 500px;
  height: 300px;
  background: #ccc;
  text-align: center;
  line-height: 300px;
}

a.control_prev, a.control_next {
  position: absolute;
  top: 40%;
  z-index: 999;
  display: block;
  padding: 4% 3%;
  width: auto;
  height: auto;
  background: #2a2a2a;
  color: #fff;
  text-decoration: none;
  font-weight: 600;
  font-size: 18px;
  opacity: 0.8;
  cursor: pointer;
}

a.control_prev:hover, a.control_next:hover {
  opacity: 1;
  -webkit-transition: all 0.2s ease;
}

a.control_prev {
  border-radius: 0 2px 2px 0;
}

a.control_next {
  right: 0;
  border-radius: 2px 0 0 2px;
}

.slider_option {
  position: relative;
  margin: 10px auto;
  width: 160px;
  font-size: 18px;
}

      button{
       background-color: white;   
          align-content: center;
      }
      
      
      #pull{
       float: right;  
          transform: rotate(90deg);

      }
    </style>

</head>
    <header><u>Music Production Empire</u><br>
     
    </header>

    
    
<body id=allOfIt>
    
    <div id='box1' class='slidingIn'>
        <div id="menuouter">
        <div id="navcontainer" align="center">
<ul id="navlist">
    <li id="active"><a href="#" id="current">Home</a></li>
<li ><a href="#">Products</a>
<ul id="subnavlist">
<li id="subactive"><a href="#" id="subcurrent">Forum</a></li>
<li><a href="#">About</a></li>
<li><a href="#">Affiliates</a></li>
<li><a href="#">Contact</a></li>
</ul>

</li>
<li><a href="#">Services</a></li>

</ul>
</div>
            </div>
        <div id="pull">  Hover</div>
        </div>
   <div id="slider">
  <a href="#" class="control_next">>></a>
  <a href="#" class="control_prev">
    <</a>
      <ul>
        <li><img src="okay.png" width="300px"height="300px">SLIDE 1</li>
        <li><img src="cry.png" width="300px"height="300px">SLIDE 2</li>
        <li><img src="cool.png" width="300px"height="300px">SLIDE 3</li>
        <li><img src="musicy.jpeg" width="300px"height="300px">SLIDE 4</li>
      </ul>
      
      <div class="slider_option">
  <input type="checkbox" id="checkbox">
  <label for="checkbox">Autoplay Slider</label>
</div>
</div>
    
       <div id="centermap" align="center">
        <p id="demo">Click the button to get your position.</p>

<button onclick="getLocation()" >Try It</button>

<div id="mapholder" ></div>
</div>
       
        <div id="theX"></div>
    

    
    <aside></aside>
    
    <div class="turntable">
        
    
       
</div>
    
        <div class="turntable2">
        
    <h1 align="center">PRO-JECT 1Xpression</h1>
            <img src="turntable.png" height="25%" width="25%"><br><a href="http://www.crutchfield.com/p_252XPS1CMG/Pro-Ject-1Xpression-Carbon-Classic-Mahogany.html"><p >Pro-Ject 1Xpression Carbon Classic details</a></img>Pro-Ject decided that it was necessary to upgrade the platter which proved to be successful. The 1Xpression Carbon Classic is finely-balanced and the platter was created using heavy aluminum. Perhaps the most innovative aspect of the platter is the middle layer that was made using Thermoplastic Elastomer (TPE) which is a phenomenal attribute. TPE restores what some resonance takes away to lower the noise floor and darken the backgrounds. The Ortofon 2M Silver Cartridge uses silver spools for optimal signal generation creating a great and precise sound. For music that sounds deep, rich, and dynamic the Pro-Jext 1Xpression Carbon Classic will fit your needs.</p>
    
    
</div>



<div class="mpctouch">
    <h1>AKAI MPC TOUCH!</h1>
    <img src="mpctouch.png" >
    <br><a href="http://www.akaipro.com/product/mpc-touch">MPC Touch details</a></img><!--<p>In creating the MPC Touch, we have once again established the iconic MPC series as the thought leader in music production technology. Combining the might of a pro-level piece of production gear truly fit to carry the MPC shield with the tactile ease of use found on smartphones and tablets, the Touch is truly a workflow revolution. How producers interact with all aspects of their sound has been forever changed. - See more at: http://www.akaipro.com/product/mpc-touch#sthash.GbbBDkBV.dpuf</p>-->
</div>  

      
     <div class="code25">
    <h1>M-AUDIO CODE 25</h1>
       <img src="code25.png" height="25%" width="25%"><br><a href="http://www.m-audio.com/products/view/code-25#.VqpYu1MrKRs">M-Audio Code 25 details</a></img><p>The Code series that has been released by M-Audio provides an almost unrivaled midi controller experience. An attractive feature on this controller is the multi-colored beat pad which does allow the user multiple banks. Precisely placed, the beat pad is left of the 25 keys. <br>
The creative potential the Code 25 comes with partially lies within the X/Y touch pad. All of your thoughts can be accomplished once you plug this into your program of choice. This midi controller comes with a copy of Software Suite although you can use this with different softwares such as: FL7, Ableton, Logic, and various other music production softwares. Let your musical aspirations be produced with clear, precise, and responsive sounds.</p>


</div>

  <div class="genelic">
    <h1>GENELIC 1038B</h1>
       <img src="genelic.png" height="25%" width="25%"><br><a href="http://www.sweetwater.com/store/detail/1038B">Genelic 1038B details</a></img><!--<p>Since 1978 Genelec has concentrated its efforts and resources into the design and manufacturing of active monitoring loudspeakers with unparalleled sonic accuracy. When first introduced, these "active" monitors were new and different. Almost three decades later, Genelec remains on the forefront of pure sound reproduction and continues to promote the concept of active monitoring, a trend in technology that many manufacturers have just begun incorporating into their products. The Genelec 1038B is a three-way active monitoring system including loudspeaker drivers, speaker enclosure, multiple power amplifiers and active, low signal level crossovers. Designed for medium sized control rooms this system is ideal for music recording studios, project studios, film and video post-production and broadcast monitoring. Mastering suites are also tailored for, where broad bandwidth, high SPL's and extended low frequency response are essential. The 1038B is designed to perform well both as a free-standing monitor and flush mounted into the control room wall.

The unique Directivity Control Waveguide (DCW) Technology used provides excellent stereo imaging and frequency balance even in difficult acoustic environments. Versatile crossover controls allow for precise matching of the speaker system to different acoustic conditions. The system can be used both in vertical and horizontal orientation by simply rotating the DCW unit. The system is very easy to use as only mains power and input signal are needed. All drivers are magnetically shielded as standard to minimize stray magnetidc field. A rack mount adapter is available so that the amplifier section can be positioned separately from the cabinet when soffit mounting. This allows for better & easier amplifier cooling and easier access to the Tone Control DIP switches during in-room system calibration.</p>-->
</div>
   
  <div class="imac">
    <h1>27" iMac w/ Retina</h1>
       <img src="imac.png" height="25%" width="25%"><br><a href="http://www.apple.com/mac/">Apple iMac w/ Retina details</a></img><!--<p>The best design. For the best performance We designed every aspect of the all-new MacBook Pro with performance in mind. The entire internal structure was built to house the very best high-performance components: all-flash storage, the latest quad-core processors, powerful discrete graphics, massive amounts of memory. Yet despite packing such an enormous amount of power into such a slim design, we still achieved an astonishing 7-hour battery life. Together, they make this MacBook Pro the world's most advanced notebook.</p>-->

</div>

<div class="bg"></div>




</body>
    
<script src="slideOut.js"></script>

    <footer>
      <!-- Primary Page Layout
  –––––––––––––––––––––––––––––––––––––––––––––––––– -->
  <div class="container">
    <div class="row">
      <div class="twelve columns">
          
           
             <form action="phpEX2.php" method="post">
  <div class="row">

          Topic: What are your favorite music production tools? <br>
<input type="radio" name="gender"
<?php if (isset($gender) && $gender=="female") echo "checked";?>
<value="female">Midi Boards<br>
<input type="radio" name="gender"
<?php if (isset($gender) && $gender=="male") echo "checked";?>
<value="male">Turntables<br>
      <input type="radio" name="gender"
<?php if (isset($gender) && $gender=="male") echo "checked";?>
<value="male">Studio Monitors<br>
      <input type="radio" name="gender"
<?php if (isset($gender) && $gender=="male") echo "checked";?>
<value="male">Computers<br>
      
  </div>
  <div class="twelve columns">
  <label for="exampleMessage">Responses and Feedback</label>
  <textarea class="u-full-width" placeholder="Hello!" name="exampleMessage"></textarea>
      
           <div class='six columns'>
      <label for='exampleRecipientInput'>Reason for contacting</label>
      <select class='u-full-width' name='messageType'>";
          
                     if ($messageType == 'Questions'){
                         echo "<option value='Questions' selected>Questions</option>";
                     } 
                 
                 if ($messageType == 'Comment'){
                         echo "<option value='Comment' selected>Comment</option>";}
          
                  if ($messageType == 'Complaint'){
                         echo "<option value='Complaint' selected>Criticism</option>"; 
                     };
              
    </div>
               
  <input class="button-primary" type="submit" value="Submit"></div>
</form>
 
             


          
          </div>   
        </div></div>
      </footer>
</html>
