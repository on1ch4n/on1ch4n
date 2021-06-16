<!DOCTYPE html>
<html lang="en">
<head>
    <link rel="sortcut icon" href="imgs/naruto_logo.png" type="image/png" />
    <meta charset="UTF-8">
	<meta http-equiv=X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=deive-width, initial-scale=1.0">
	
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
	<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css">
	<title> JOGO DA VELHA NARUTO </title>
	<style>
		.preload {
			position: fixed;
            z-index: 99999;
			top: 0;
			left: 0;
            width: 100%;
            height: 100%;
			opacity: 1;
			background-image: url('https://38.media.tumblr.com/bec5933eea5043acf6a37bb1394384ab/tumblr_meyfxzwXUc1rgpyeqo1_400.gif');
			background-color: #fff;
			background-size: 298px 298px;
			background-position: center;
			background-repeat: no-repeat;
		}	
	    body{
		    background: url('imgs/homescreen.png') no-repeat center center fixed;
			position: static;
			-webkit-background-size: cover;
			-moz-background-size: cover;
			background-size: cover;
			-o-background-size: cover;
		}
		.rodape{
		    color: black;
		    padding-top: 230px;
		}	
		.logo{
			padding-top: 40px;
		}

		.menu a:link{
		    color: white;
			text-decoration: none;
			text-shadow: 2px 2px black;
		}	
		.menu a:hover{
		    color: red;
			text-decoration: none;
			text-shadow: 2px 2px black;
		}	
		.menu{
		padding-top: 40px
		}
		
    </style>		
</head>
<body>

    <audio autoplay>
        <source src="sounds/jutsu_sound_effect.wav" type="audio/mpeg">
    </audio>

	<audio controls autoplay loop>
	    <source src="musics/naruto_flauta.wav" type="audio/mpeg">
	</audio>	
	
	<div id="preload" class="preload"></div>


    <div class="container-fluid">

        <div class="row logo">
            <div class="col-md-12">
                <center>
                    <img class="img-responsive" src="imgs/logo.png" alt="Logo do Jogo">
			    </center>
		    </div>
	    </div>
	
        <div class="row menu">
        	<div class="col-md-12">
			    <center>
				    <a href="">
					    <h1 class="visible-md-block visible-lg-block link-effect">INICIAR</h1>
						<h3 class="visible-sm-block visible-xs-block link-effect">INICIAR</h3>
					</a>	
                    <a href="index2.html">
					    <h1 class="visible-md-block visible-lg-block link-effect">CRÉDITOS</h1>
						<h3 class="visible-sm-block visible-xs-block link-effect">CRÉDITOS</h3>
					</a>
				</center>
			</div>	
		</div>

        <div class="row rodape">
            <div class="col-md-12">
                <center>
                    <p class="visible-md-block visible-lg-block">Desktop Version v.1.0.6</p>
					<p class="visible-sm-block visible-xs-block">Mobile Version v.2.7.4</p>
				</center>
			</div>
		</div>	
		
		
	</div>


<script src="https://ajas.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
<script src="https://code.jquery.com/jquery-3.5.0.js"></script>
<script>
    $(document).ready(function() {

	    $(".link-effect").on("mouseenter", function() { 
            hoverElem = this; 
            $(this).addClass("animate__animated animate__shakeX");
        });

        $(".link-effect").on("mouseleave", function() {
            hoverElem = this; 
            $(this).removeClass("animate__animated animate__shakeX");
        });
	
	    $(".link-effect").click(function () {
           var audio = {};
           audio["walk"] = new Audio();
           audio["walk"].src = "sounds/jutsu_sound_effect.wav"
           audio["walk"].addEventListener('load', function () {
           audio["walk"].play();
        });
    });

});
$(document).ready(function(){
          setTimeout('$("#preload").fadeOut(100)', 1500);
       
      });
</script>
</body>
</html>
