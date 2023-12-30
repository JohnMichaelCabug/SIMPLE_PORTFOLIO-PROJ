<!DOCTYPE html>
<html lang="en">
  <head>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" />
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" />
    <meta charset="UTF-8">
    
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MY PERSONAL PORTFOLIO</title>
    <style>
      body {
        font-family: "Lucida Console", "Courier New", monospace;
        background-color: #24201d;
        color: rgb(19, 16, 12);
        margin: 45px;
        text-align: center;
        transition: background-color 0.5s;
        min-height: 130vh;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
      }

      header {
        background: url('https://media.giphy.com/media/BHNfhgU63qrks/giphy.gif') center center/cover fixed;
        padding: 15px;
        text-align: center;
        letter-spacing: 30px;
        position: relative;
        transition: background 0.5s;
        box-shadow: 5 10 20px rgba(255, 165, 0, 0.8);
        font-family: "arial", cursive;
        top: 0;
        position: sticky;
        z-index: 1000;
      }

      .image-slider-container {
        display: flex;
        justify-content: center;
        overflow: hidden;
        margin-top: 40px;
        max-width: 600px;
        margin: 0 auto;
      }

      .image-slide {
        flex: 0 0 150px;
        margin-right: 5px;
        transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
      }

      .image-slide:hover {
        transform: scale(0.8);
        box-shadow: 0 0 30px rgb(240, 10, 10);
      }

      .image-slide img {
        width: 100%;
        height: auto;
        border-radius: 5px;
      }

      @media screen and (max-width: 800px) {
        .image-slider-container {
          flex-direction: column;
          align-items: center;
          max-width: 200%;
        }

        .image-slide {
          margin-right: 0;
          margin-bottom: 10px;
        }
      }

      

      header h1 {
        text-shadow: 0 0 20px rgba(255, 165, 0, 1);
      }

      nav {
        display: flex;
        justify-content: space-around;
        background-color: #0b0b07;
        flex-direction: flex-start;
        padding: 10px;
      }

      nav a {
        color: #fff;
        text-decoration: none;
        font-weight: bold;
        transition: color 0.3s;
      }

      nav a:hover {
        color: #0f0c08;
        background-image: url('https://media.giphy.com/media/WrHrrwqxCTTb7uKQQX/giphy.gif');
        color: black;
        padding: 16px 32px;
        text-align: center;
        font-size: 16px;
        margin: 4px 2px;
        transition: 0.5s;
      }

      .centered-content {
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: center;
      }

      .centered-content img {
        width: 200px;
        height: 200px;
        border-radius: 50%;
        margin-top: 10px;
        transition: box-shadow 0.3s, transform 0.3s;
      }

      .centered-content img:hover {
        box-shadow: 0 0 20px 5px rgba(255, 165, 0, 1);
        transform: rotate(360deg);
      }

      .centered-content hr {
        height: 40%;
        width: 2px;
        background-color: orangered;
        margin: 10px;
      }

      .description-box {
        background: linear-gradient(45deg, #ff5e00, #ff8b38);
        color: rgb(201, 170, 170);
        padding: 10px;
        margin: 10px;
        border-radius: 5px;
        box-shadow: 0 0 10px rgba(255, 165, 0, 0.8);
        overflow: hidden;
        text-align: center;
        position: relative;
      }

      .right-description {
        background-color: transparent;
        color: rgb(224, 89, 10);
        padding: 10px;
        margin: 10px;
        border-radius: 10px;
        max-width: 800px;
        max-height: 120px;
        white-space: nowrap;
        overflow: hidden;
        font-size: 20px;
        font-weight: bold;
        font-family: arial;
        letter-spacing: 2px;
        animation: typing 5s steps(40) infinite;
      }

      @keyframes typing {
  from {
    width: 0%;
  }

  to {
    width: 100%;
  }
}
      .fas:hover {
    animation: glowing 1s infinite;
  }

  @keyframes glowing {
    0% {
      color: #b305f8;
      text-shadow: 0 0 10px #d87c04, 0 0 20px #16d804, 0 0 30px #9209ee;
    }
    50% {
      color: #04fcd2;
      text-shadow: 0 0 20px #ffbf00, 0 0 30px #ffbf00, 0 0 40px #ffbf00;
    }
    100% {
      color: #20f73d;
      text-shadow: 0 0 10px #d87c04, 0 0 20px #d87c04, 0 0 30px #d87c04;
    }
  }

      .centered-content img {
        width: 220px;
        height: 220px;
        border-radius: 50%;
        margin-top: 10px;
        transition: box-shadow 0.3s, transform 0.3s;
      }

      .centered-content img:hover {
        box-shadow: 0 0 30px 10px rgba(255, 165, 0, 1);
        transform: rotate(360deg);
      }

      .social-icons {
        display: flex;
        justify-content: center;
        width: 100%;
      }

      .social-icons a {
        color: #f8f6f5;
        text-decoration: none;
        margin: 0 15px;
        font-size: 20px;
        transition: transform 0.3s, color 0.3s, background 0.3s;
        position: relative;
      }

      .social-icons i {
        margin-right: 10px;
      }

      .social-icons a:hover {
        transform: translateY(-9px);
        color: #fff;
        background: linear-gradient(45deg, #ff5e00, #ff8b38);
        box-shadow: 0 0 20px 5px rgba(255, 165, 0, 1);
      }

      .additional-content {
        background-color: #0b0b07;
        color: #fff;
        padding: 20px;
        text-align: center;
        font-family: arial;
      }

      .glowing-text {
        color: #d35b0b;
        font-size: 14px;
        font-weight: bold;
        font-family: 'arial';
        text-shadow: 0 0 10px rgb(100, 94, 59), 0 0 20px rgb(212, 212, 212), 0 0 30px rgba(255, 215, 0, 1);
      }
    </style>
  </head>
  <body>
    <header>
      <input type="text" class="search-bar" placeholder="Search...">
      <h1 style="color: #fff;">JOHN MICHAEL PH</h1>
    </header>
    <script>
      document.addEventListener("DOMContentLoaded", function () {
        const searchBar = document.querySelector(".search-bar");

        searchBar.addEventListener("keydown", function (event) {
          if (event.key === "Enter") {
            const query = searchBar.value.trim();
            if (query !== "") {
              // Use Google as the search engine, you can change the URL as needed
              const searchURL = `https://www.google.com/search?q=${encodeURIComponent(
                query
              )}`;
              window.location.href = searchURL;
            }
          }
        });
      });
    </script>
    <nav>
      <a href="#home">Home</a>
      <a href="#contact">Contact</a>
      <a href="#about Me">About Me</a>
    </nav>
    <div class="centered-content">
      <hr>
      <img src="bgmyprof.png" alt="Circle Image">
      <div class="right-description">
        <p>HI I'm John Michael Cabug 19 Years of age BS-IT 1ST YEAR</p>
      </div>
    </div>
    
    </div>
    <div class="social-icons">
      <a href="https://web.facebook.com/profile.php?id=61552504828926" target="_blank">
        <i class="fab fa-facebook"></i> Facebook </a>
      <a href="https://www.instagram.com/notfound_jm00/" target="_blank">
        <i class="fab fa-instagram"></i> Instagram </a>
      <a href="https://www.youtube.com/channel/UCVUbpwx2uBZ3PwWtaV15CQQ" target="_blank">
        <i class="fab fa-youtube"></i> YouTube </a>
      <a href="https://www.tiktok.com/@jm.pdf8?_t=8i7R4LRAU9i&_r=1&fbclid=IwAR3dt3dd_Q2d20dX_3bScIsN6UA41lG4EfcndBMfyu-MfU4ZW8TmkqG2JGE" target="_blank">
        <i class="fab fa-tiktok"></i> Tiktok </a>
    </div>
    <div class="glowing-text">
      </h2>
      <h2>MY FEATURED ACTIVITY </h2>
      <div class="image-slider-container">
        <div class="image-slide">
          <img src="pic06.jpg" alt="Image 1">
          <p>SERVE THE BALL</p>
        </div>
        <div class="image-slide">
          <img src="222.jpg" alt="Image 2">
          <p>SHADE</p>
        </div>
        <div class="image-slide">
          <img src="pic05.jpg" alt="Image 3">
          <p>BOUNCE THE BALL</p>
        </div>
        <div class="image-slide">
          <img src="333.jpg" alt="Image 4">
          <img src="444.jpg" alt="Image 4">
          <p>EXTRA INCOME HAHA</p>
        </div>
      </div>
      </div>
    </div>
  </div>
</div>
      



<audio id="buttonAudio" preload="auto">
  <source src="Rick Astley - Never Gonna Give You Up (Official Music Video).mp3" type="audio/mp3">
  <source src="George Michael - Careless Whisper (Lyric Video).mp3" type="audio/mp3">
  <source src="Wham! - Wake Me Up Before You Go-Go (Official Video).mp3" type="audio/mp3">
  <source src="Put Your Head On My Shoulder.mp3" type="audio/mp3">
</audio>

    </div>
    <div class="button-container">
      <i id="prevButton" class="fas fa-step-backward" onclick="prevMusic()"></i>
      <i id="playButton" class="fas fa-play" onclick="playMusic()"></i>
      <i id="nextButton" class="fas fa-step-forward" onclick="nextMusic()"></i>
    </div>
  
    </script>
    <script>
      var audio = document.getElementById('buttonAudio');
      var playButton = document.getElementById('playButton');
      var nextButton = document.getElementById('nextButton');
      var prevButton = document.getElementById('prevButton');
      var currentTrack = 0;
    
      function playMusic() {
    if (audio.paused) {
      audio.play();
      playButton.innerHTML = 'Pause';
    } else {
      audio.pause();
      playButton.innerHTML = 'Play';
    }
  }

  function nextMusic() {
    currentTrack = (currentTrack + 1) % audio.children.length;
    changeTrack();
  }

  function prevMusic() {
    currentTrack = (currentTrack - 1 + audio.children.length) % audio.children.length;
    changeTrack();
  }

  function changeTrack() {
    audio.src = audio.children[currentTrack].src;
    audio.play();
    playButton.innerHTML = 'Pause';
  } 
    </script>
   <script>
    document.addEventListener("DOMContentLoaded", function () {
      const body = document.body;
  
      body.addEventListener("mousemove", (e) => {
        const mouseX = e.clientX;
        const mouseY = e.clientY;
  
        const panUpCursor = document.createElement("div");
        panUpCursor.className = "pan-up-cursor";
        panUpCursor.style.left = `${mouseX}px`;
        panUpCursor.style.top = `${mouseY}px`;
  
        const randomColor1 = Math.floor(Math.random() * 255);
        const randomColor2 = Math.floor(Math.random() * 255);
        const randomColor3 = Math.floor(Math.random() * 255);
        const gradientColor = `rgb(${randomColor1},${randomColor2},${randomColor3})`;
  
        panUpCursor.style.backgroundImage = `radial-gradient(circle, ${gradientColor}, transparent)`;
        body.appendChild(panUpCursor);
  
        body.appendChild(panUpCursor);
  
        setTimeout(() => {
          panUpCursor.remove();
        }, 200);
      });
    });
  </script>
  
  
    
    
    </div>
    </div>
    </div>
    </div>
    </div>
    <div class="blurred-description-box">
      <div class="blurred-content">
        <p>I'm John Michael Cabug, a first-year college student,and i'm currently pursuing a Bachelor of Science in Information Technology(BS-IT). Eager to explore the realm of technology, I navigate the exciting journey but stressful hehe of acadimia with curiosity and dedication. I combine my passion for IT with a commitment to learning. </p>
      </div>
      <div class="contact-section">
        <div class="contact-content">
          <h2>Contact Information</h2>
          <div class="contact-info">
            <a href="johncabug@gmail.com" target="_blank">Send Email</a>
            <a href="09754778428">Phone</a>
            <a href="https://maps.app.goo.gl/GzjKkKLHkRt4VMwR9" target="_blank">Address</a>
          </div>
        </div>
      </div>
      
      <div class="rating">
        <input type="radio" id="star5" name="rating" value="5">
        <label for="star5">★</label>
        <input type="radio" id="star4" name="rating" value="4">
        <label for="star4">★</label>
        <input type="radio" id="star3" name="rating" value="3">
        <label for="star3">★</label>
        <input type="radio" id="star2" name="rating" value="2">
        <label for="star2">★</label>
        <input type="radio" id="star1" name="rating" value="1">
        <label for="star1">★</label>
      </div>
      <label for="rating">Can You Rate My Portfolio</label>
      <div class="rating"></div>
    </div>
    </div>  

    <div>
    </div>
    <style>
    .search-bar {
   background: url('https://media.giphy.com/media/hFhygTRHt4jvGQo52q/giphy.gif');
   background-size: cover;
   color: #0f0e0e;
   border: none;
   padding: 10px;
   border-radius: 5px;
   transition: box-shadow 0.3s, background-color 0.3s;
   font-size: 16px;
   font-family: arial;
   position: absolute;
   top: 15px;
   right: 15px;
}
.search-bar:hover {
  background-color: #0ebbb2; 
  box-shadow: 0 0 20px rgb(102, 100, 96); 
}
@media screen and (max-width: 600px) {
  .search-bar {
    top: 5px;
    right: 5px;
    width: 20%; 
    height: auto;
    
  }

  header {
    letter-spacing: 10px;
    
  }

  nav {
    flex-direction: column;
    align-items: center;
  }

  nav a {
    padding: 10px;
    font-size: 14px;
  }

  .centered-content img {
    width: 150px;
    height: 150px;
  }

  .right-description {
    font-size: 16px;
  }
}



header {
  position: sticky;
  z-index: 1000;
  top: 0;
}
      
      
.button-container {
  display: flex;
  justify-content: space-around;
  margin-top: 10px;
}


.button-container i {
  font-size: 24px; 
  cursor: pointer;
  transition: transform 0.3s, color 0.3s;
}

.button-container i:hover {
  transform: translateY(-5px);
  color: #d87c04;
}
.pan-up-cursor {
    position: fixed;
    width: 10px;
    height: 10px;
    background-color: #fff;
    border-radius: 50%;
    pointer-events: none;
    animation: panUp 0.5s infinite alternate;
    z-index: 9999;
  }

  @keyframes panUp {
    from {
      transform: translateY(0);
    }
    to {
      transform: translateY(-10px);
    }
  }


      .blurred-description-box {
        background: url('https://media.giphy.com/media/9JxkPTP3alOykb8PmQ/giphy.gif') center center/cover fixed;
        padding: 20px;
        margin: 20px;
        border-radius: 10px;
        transition: box-shadow 0.3s, transform 0.3s;
      }

      .blurred-description-box:hover {
        box-shadow: 0 0 20px rgba(255, 165, 0, 1);
        transform: scale(1.05);
      }

      .blurred-content {
        text-align: center;
        transition: font-weight 0.3s;
      }

      .blurred-description-box:hover .blurred-content {
        font-weight: bold;
        text-shadow: 0 0 10px rgba(255, 165, 0, 1);
        font-family: arial;
      }

      .blurred-content {
        text-align: center;
      }

      .contact-section {
        position: relative;
        margin-top: 20px;
      }

      .contact-content {
        background: #0b0b07;
        color: #fff;
        padding: 20px;
        border-radius: 10px;
        transform: translateZ(10px);
        box-shadow: 0 0 20px rgba(255, 165, 0, 0.8);
        transition: transform 0.3s, box-shadow 0.3s;
      }

      .contact-content:hover {
        transform: translateZ(20px);
        box-shadow: 0 0 30px rgba(255, 165, 0, 1);
      }

      .contact-info {
        display: flex;
        justify-content: space-around;
        flex-wrap: wrap;
      }

      .contact-info a {
        color: #fff;
        text-decoration: none;
        transition: color 0.3s;
      }

      .contact-info a:hover {
        color: #d87c04;
      }

      @media screen and (max-width: 600px) {
        body {
          margin: 15px;
        }

        header {
          letter-spacing: 10px;
          background-color: green;
        }

        nav {
          flex-direction: column;
          align-items: center;
        }

        nav a {
          padding: 10px;
          font-size: 14px;
        }

        .centered-content img {
          width: 150px;
          height: 150px;
        }

        .right-description {
          font-size: 16px;
        }

        @media screen and (min-width: 601px) and (max-width: 1024px) {
          body {
            color: gray;
          }

          @media screen and (min-width: 1025px) and (max-width: 1440px) {
            body {
              color: black;
            }

            @media screen and (min-width: 1441px) {}
    </style>
    <style>
      
      .bottom-row {
        display: flex;
        justify-content: space-around;
        margin: 20px;
      }

      .box {
        width: 120px;
        height: 120px;
        background-color: #000000;
        color: #fff;
        display: flex;
        align-items: center;
        justify-content: center;
        font-weight: bold;
        cursor: pointer;
        transition: background-color 0.3s;
      }
      }

      footer {
        background-color: #0b0b07;
        color: #fff;
        padding: 10px;
        text-align: center;
        position: relative;
        margin-top: auto;
      }

      .footer-icons {
        display: flex;
        justify-content: center;
        margin-top: 10px;
      }

      .footer-icons a {
        color: #fff;
        text-decoration: none;
        margin: 0 10px;
        font-size: 20px;
        transition: transform 0.3s, color 0.3s;
        position: relative;
      }

      .footer-icons i {
        margin-right: 5px;
      }

      .footer-icons a:hover {
        transform: translateY(-5px);
        color: #d87c04;
      }

      .glowing-footer {
        color: #d35b0b;
        font-size: 14px;
        font-weight: bold;
        font-family: 'arial';
        text-shadow: 0 0 10px rgb(100, 94, 59), 0 0 20px rgb(212, 212, 212), 0 0 30px rgba(255, 215, 0, 1);
      }

      .rating {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: 20px;
      }

      .rating input {
        display: none;
      }

      .rating label {
        font-size: 30px;
        color: #fff;
        cursor: pointer;
      }

      .rating label:hover,
      .rating label:hover~label {
        color: #d87c04;
      }

      .rating input:checked~label {
        color: #d87c04;
      }
      .button-container {
  display: flex;
  justify-content: space-around;
  margin-top: 20px;
}

.button-container button {
  background-color: #d87c04;
  color: #fff;
  padding: 16px 32px;
  text-align: center;
  font-size: 16px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  position: relative;
  overflow: hidden;
  transition: transform 0.3s, box-shadow 0.3s, background-color 0.3s;
}

.button-container button:hover {
  transform: translateY(-5px);
  box-shadow: 0 0 20px rgba(255, 165, 0, 1);
  background-color: #0f0c08;
}

.button-container button::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(45deg, #ff5e00, #ff8b38);
  transform: perspective(500px) rotateX(45deg) scale(0, 0.5);
  transform-origin: 0% 100%;
  transition: transform 0.3s;
}

.button-container button:hover::before {
  transform: perspective(500px) rotateX(45deg) scale(1, 1);
}

    </style>
    <footer>
      <div class="footer-icons">
        <a href="https://web.facebook.com/profile.php?id=61552504828926" target="_blank">
          <i class="fab fa-facebook"></i>
          <!-- Facebook icon -->
        </a>
        <a href="https://www.instagram.com/notfound_jm00/" target="_blank">
          <i class="fab fa-instagram"></i>
          <!-- Instagram icon -->
        </a>
        <a href="https://www.youtube.com/channel/UCVUbpwx2uBZ3PwWtaV15CQQ" target="_blank">
          <i class="fab fa-youtube"></i>
          <!-- YouTube icon -->
        </a>
        <a href="https://www.tiktok.com/@jm.pdf8?_t=8i7R4LRAU9i&_r=1&fbclid=IwAR3dt3dd_Q2d20dX_3bScIsN6UA41lG4EfcndBMfyu-MfU4ZW8TmkqG2JGE" target="_blank">
          <i class="fab fa-tiktok"></i>
          <!-- TikTok icon -->
        </a>
      </div>
      <div class="glowing-footer"> © 2023 John Michael PH. All rights reserved. </div>
    </footer>
  </body>
</html>
