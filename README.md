# IdentificationCard
Design of my Identification Card as Web Developer
HTML:
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <script src="https://kit.fontawesome.com/dd8c49730d.js" crossorigin="anonymous"></script>
  <link rel="stylesheet" href="escritorioncrm.css">
  <title>DEKSTOP CRM</title>
</head>

<body>

<div class="background"></div>

<div class="outer-div">
  <div class="inner-div">
    <div class="front">
      <div class="front__bkg-photo"></div>
      <div class="front__face-photo"></div>
      <div class="front__text">
        <h3 class="front__text-header">I am Web Developer</h3>
        <p class="front__text-para"><i class="fas fa-map-marker-alt front-icons"></i>Earth</p>
        
        <span class="front__text-hover">Hover For Details</span>
      </div>
    </div>
    <div class="back">
      <div class="social-media-wrapper">
        <a href="#" class="social-icon"><i class="fab fa-youtube" aria-hidden="true"></i></a> 
        <a href="#" class="social-icon"><i class="fab fa-github" aria-hidden="true"></i></a>
        <a href="#" class="social-icon"><i class="fab fa-twitter" aria-hidden="true"></i></a>
         <a href="#" class="social-icon"><i class="fab fa-instagram" aria-hidden="true"></i></a>
      </div>
    </div>

  </div>
</div>
  </body>
</html>






CSS:
body {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: robato;
}

.background {
  position: absolute;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100vw;
  background: url("https://images.unsplash.com/photo-1447433589675-4aaa569f3e05?ixlib=rb-0.3.5&s=4222852e25e0f57d9485f7889957e99a&auto=format&fit=crop&w=2000&q=80");
  background-size: cover;
  background: #000;
  background-position: 0 50%;
}

.background:after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background: rgba(0, 0, 0, 0);
}

.outer-div,
.inner-div {
  height: 450px;
  max-width: 300px;
  margin: 0 auto;
  position: relative;
}

.outer-div {
  perspective: 900px;
  perspective-origin: 50% calc(50% - 18em);
}

.inner-div {
  margin: 0 auto;
  border-radius: 5px;
  font-weight: 400;
  color: #071011;
  font-size: 1rem;
  text-align: center;
  transition: all 0.6s cubic-bezier(0.8, -0.4, 0.2, 1.7);
  transform-style: preserve-3d;
}

.inner-div:hover .social-icon {
  opacity: 1;
  top: 0;
}

.outer-div:hover .inner-div {
  transform: rotateY(180deg);
}

.front,
.back {
  position: relative;
  top: 0;
  left: 0;
  -webkit-backface-visibility: hidden;
          backface-visibility: hidden;
}

.front {
  cursor: pointer;
  height: 100%;
  background: orange;
  -webkit-backface-visibility: hidden;
          backface-visibility: hidden;
  border-radius: 35px;
  box-shadow: 0 15px 10px -10px rgba(0, 0, 0, 0.5), 0 1px 4px rgba(0, 0, 0, 0.3), 0 0 40px rgba(0, 0, 0, 0.1) inset;
}

.front__bkg-photo {
  position: relative;
  height: 220px;
  width: 300px;
  background: url("https://images.unsplash.com/photo-1511207538754-e8555f2bc187?ixlib=rb-0.3.5&ixid=eyJhcHBfaWQiOjEyMDd9&s=88672068827eaeeab540f584b883cc66&auto=format&fit=crop&w=1164&q=80") no-repeat;
  background-size: cover;
  -webkit-backface-visibility: hidden;
          backface-visibility: hidden;
  overflow: hidden;
  border-top-right-radius: 5px;
  border-top-left-radius: 5px;
}

.front__bkg-photo:after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
}

.front__face-photo {
  position: relative;
  top: -60px;
  height: 120px;
  width: 190px;
  margin: 0 auto;
  border-radius: 50%;
  border: 3px solid #000;
  background: url("img/laptop.jpg") no-repeat;
  background-size: cover;
  overflow: hidden
}

.front__text {
  position: relative;
  top: -55px;
  margin: 0 auto;
  font-family: "robato";
  font-size: 28px;
  -webkit-backface-visibility: hidden;
          backface-visibility: hidden;
}

.front__text .front__text-header {
  font-weight: 700;
  font-family: "robato";
  text-transform: uppercase;
  font-size: 23px;
}

.front__text .front__text-para {
  position: relative;
  top: -3px;
  color: blue;
  font-size: 14px;
  letter-spacing: 0.4px;
  font-weight: 400;
  font-family: "robato", sans-serif;
}

.front__text .front-icons {
  position: relative;
  top: 0;
  font-size: 14px;
  margin-right: 6px;
  color: gray;
}

.front__text .front__text-hover {
  position: relative;
  top: 10px;
  font-family: robato;
  font-size: 14px;
  color: tomato;
  -webkit-backface-visibility: hidden;
          backface-visibility: hidden;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.4px;
  border: 2px solid black;
  padding: 8px 15px;
  border-radius: 30px;
  background: tomato;
  color: blue;
}

.back {
  transform: rotateY(180deg);
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-color: #071011;
  border-radius: 25px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.social-media-wrapper {
  font-size: 36px;
}

.social-media-wrapper .social-icon {
  position: relative;
  top: 20px;
  margin-left: 5px;
  margin-right: 5px;
  opacity: 0;
  color: orange;
  transition: all 0.4s cubic-bezier(0.3, 0.7, 0.1, 1.9);
}

.social-media-wrapper .social-icon:nth-child(1) {
  transition-delay: 0.6s;
}
.social-media-wrapper .social-icon:nth-child(2) {
  transition-delay: 0.7s;
}
.social-media-wrapper .social-icon:nth-child(3) {
  transition-delay: 0.8s;
}
.social-media-wrapper .social-icon:nth-child(4) {
  transition-delay: 0.9s;
}

.fab {
  position: relative;
  top: 0;
  left: 0;
  transition: all 200ms ease-in-out;
}

.fab:hover {
  top: -5px;
}
