<!DOCTYPE html>
<html><head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>The Hub</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Space+Mono&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;700&display=swap');
    body {
      font-family: 'Space Mono', monospace;
      font-size: 14px;
      background-color: #f2f2f2;
      color: #333333;
      margin: 0;
      padding: 0;
    }
    header {
      background: linear-gradient(to bottom, #00b3b3, #008080);
      padding: 40px 20px;
      text-align: center;
      position: relative;
    }
    header h1 {
      font-size: 45px;
      color: #ffffff;
      margin: 0;
    }
    .social {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
    }
    .social div {
      margin-bottom: 5px;
    }
    .social div a {
      display: flex;
      align-items: center;
      text-decoration: none;
      color: black;
    }
    .social div a img {
      width: 15px;
      height: 15px;
    }.login {
      position: absolute;top: 14px;
      right: 14px;
      display: flex;
      align-items: center;
      font-weight: bold;
      text-decoration: none;
}
.login a {
  color: yellow !important;
}
.login:hover .tooltip {
  visibility: visible;
  opacity: 1;
}
.tooltip {
  position: absolute;
  top: 75%;
  right: 35%;
  width: 200px;
  background-color: #f9f9f9;
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 10px;
  font-size: 14px;
  color: black;
  text-align: center;
  visibility: hidden;
  opacity: 0;
  transition: visibility 0s, opacity 0.3s ease-in-out;
}.hub-card {
      background: linear-gradient(to bottom, #008080, #00b3b3);
      border-radius: 10px;
      border: 2px solid #ffffff;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
      padding: 10px;
      text-align: center;
      max-width: 210px;
      width: 45%;
      margin: 0 auto;
      margin-top: -140px;
      position: relative;
      z-index: 2;
    }
    .hub-card h1 {
      font-size: 16px;
      margin-top: 0;
      margin-bottom: 2px;
      color: #ffffff;
    }
    .hub-card p {
      font-size: 14px;
      margin-bottom: 2px;
      color: #ffffff;
    }
    .dropdown-container {
  text-align: center;
  margin-top: 4px;
}
.dropdown {
  display: inline-block;
  position: relative;
}
.dropdown select {
  font-family: 'Space Mono', monospace;
  font-size: 10px;
  padding: 5px 5px;
  border-radius: 5px;
  border: 2px solid #ffffff;
  background-color: #008080;
  color: #ffffff;
  appearance: none;
  outline: none;
  background-image: url('https://img.icons8.com/material-rounded/12/ffffff/keyboard-arrow-down--v1.png');
  background-repeat: no-repeat;
  background-position: right center;
  background-origin: content-box;
  cursor: pointer;
}
    .graffiti {
            position: absolute;
            transform: translate(-50%, -50%);
            font-family: 'Space Mono', monospace;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            z-index: 1;
            left: 10px;
            font-size: 10px;
            transform: rotate(-7deg);
            top: 10%;
            color: white;
        }
        .box {
            display: inline-block;
            padding: 1px;
            border: 1px solid #E53E3E;
            background-color: transparent;
        }
        .box a {
            color: white;
            text-decoration: none;
        }
    .container {
      position: relative;
      width: 150px;
      height: 200px;
      margin: 20px auto;
    }
    .triangle {
      position: absolute;
      top: 50%;
      left: 40.5%;
      transform: translate(-50%, -50%);
      width: 0;
      height: 0;
      border-left: 30px solid transparent;
      border-right: 30px solid transparent;
      border-bottom: 60px solid #00b3b3;
      transition: all 1s ease;
    }
    #left-triangle {
      top: calc(50% - 30px);
      left: calc(50% - 60px);
      border-bottom-color: #008c8c;
    }
    #right-triangle {
      top: calc(50% + 30px);
      left: calc(50% - 60px);
      border-bottom-color: #00a6a6;
    }
    #center-triangle:hover {
      transform: translate(-50%, -50%) rotate(180deg) translateY(5px);
    }
    #center-triangle:hover ~ #left-triangle {
      transform: translate(-50%, -50%) translateX(46px) translateY(2px);
    }
    #center-triangle:hover ~ #right-triangle {
      transform: translate(-50%, -50%) translateX(46px) translateY(-58px);
    }
    .reflect-text {
      position: absolute;
      top: 49%;
      left: 60%;
      transform: translate(-50%, -50%) rotate(65deg);
      font-size: 13px;
      font-weight: bold;
      color: transparent;
      background: linear-gradient(45deg, red, orange, yellow, green, blue, indigo, violet, red);
      background-clip: text;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      transition: all 1s ease;
      z-index: 2;
    }
    .reflection {
      position: absolute;
      top: 70%;
      left: 43%;
      transform: translate(-50%, -50%) rotate(0.1deg);
      font-size: 13px;
      font-weight: bold;
      color: transparent;
      background: linear-gradient(45deg, red, orange, yellow, green, blue, indigo, violet, red);
      background-clip: text;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      transition: all 1s ease;
      z-index: 2;
    }
    #center-triangle:hover ~ .reflect-container .reflect-text {
      transform: translate(-50%, -50%) translateX(-25px) translateY(-45px) rotate(0.1deg);
    }
    #center-triangle:hover ~ .reflect-container .reflection {
      transform: translate(-50%, -50%) translateX(-2px) translateY(-28px);
    }
    .reflect-container:hover .reflection {
      opacity: 0.8;
    }
    .new-page-link {
      position: absolute;
      top: 40%;
      left: 40%;
      transform: translate(-50%, -50%);
      font-size: 11px;
      font-weight: bold;
      color: yellow;
      text-decoration: none;
      z-index: 3;
      display: none;
    }
    .container:hover .new-page-link {
      display: block;
    }
    .community-container {
      color: #00b3b3;
      text-align: center;
      position: relative;
      margin-bottom: 100px;
    }
    .community-heading,
    .community-description,
    .community-benefits,
    .community-cta,
    .community-benefits-list {
      color: #00b3b3;
      text-align: center;
    }
    .community-heading {
      font-size: 18px;
      margin-top: 20px;
    }
    .community-description {
      font-size: 14px;
      margin-bottom: 10px;
    }
    .community-benefits {
      font-size: 14px;
      font-weight: bold;
    }
    .community-benefits-list {
      margin-top: 5px;
      list-style-type: disc;
      margin-left: 15px;
      font-size: 17px;
    }
    .community-cta {
      font-style: italic;
      margin-top: 10px;
      font-size: 17px;
    }
    .grid-container {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      grid-gap: 20px;
      background: linear-gradient(to bottom, #00b3b3, #ffffff);
      border-radius: 10px;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
      padding: 15px;
      justify-items: center;
    }
    .grid-item {
      background-color: #00b3b3;
      color: #ffffff;
      border-radius: 10px;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2), 0 6px 6px rgba(0, 0, 0, 0.2);
      padding: 10px;
      text-align: center;
      position: relative;
      overflow: hidden;
      transition: transform 0.3s, box-shadow 0.3s;
      cursor: pointer;
      width: 100%;
    }
    .grid-item:hover {
      transform: translateY(-3px);
      box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3), 0 8px 8px rgba(0, 0, 0, 0.3);
    }
    .grid-item .hover-text {
      display: none;
      font-size: 10px;
    }
    .grid-item:hover .hover-text {
      display: block;
    }
    footer {
      background: linear-gradient(to bottom, #ffffff, #00b3b3);
      padding: 35px;
      color: #ffffff;
      text-align: center;
      font-size: 14px;
    }
    .footer-container {
      max-width: 1200px;
      margin: 0 auto;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-wrap: wrap;
    }
    .footer-container .box {
      background-color: #00b3b3;
      color: #ffffff;
      border-radius: 10px;
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2), 0 6px 6px rgba(0, 0, 0, 0.2);
      padding: 10px;
      text-align: center;
      margin: 10px;
      cursor: pointer;
    }
    .footer-container .box h3 {
      margin: 0;
    }
    .footer-container p {
      margin-top: 10px;
    }
    .footer-container input[type="text"] {
      width: 100%;
      padding: 5px;
      border-radius: 5px;
      border: none;
      background-color: #008080;
      color: #ffffff;
      margin-top: 5px;
    }
    @media (max-width: 768px) {
      header h1 {
        font-size: 30px;
      }
      .hub-card {
        width: 90%;
      }
    }
    @media (max-width: 480px) {
      header h1 {
        font-size: 25px;
      }
      .hub-card {
        width: 100%;
      }
      .grid-container {
        grid-template-columns: repeat(2, 1fr);
      }
    }
  </style>
<script async src="https://www.googletagmanager.com/gtag/js?id=G-RZG8MP5HRX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-RZG8MP5HRX');
</script>
</head>
<body>
<header>
  <div class="graffiti">
        This is your Hub !<br>
        Do you want to change It ?<br>
        Submit Request <br>
        <span class="box"><a href="https://docs.google.com/forms/d/e/1FAIpQLScrHwrJjCwCha1DkU4ZNGvWP2zR41vlqTsyVuK-prMGZjFgQQ/viewform?embedded=true" target="_blank">Here</a></span>
    </div>
  <div class="login">
  <a href="#">Login</a><div class="tooltip">
    You don't need to Sign Up! You are already a Member of Our Community. Save that time browsing what's on offer this week!
  </div>
</div>
    <h1>Collabor8</h1>
    <div class="social">
      <div>
        <a href="#">
          <img src="https://img.icons8.com/office/30/FF0000/youtube.png" alt="YouTube">
        </a>
      </div>
      <div>
        <a href="#">
          <img src="https://img.icons8.com/office/30/FF0000/facebook-new.png" alt="Facebook">
        </a>
      </div>
      <div>
        <a href="#">
          <img src="https://img.icons8.com/office/30/FF0000/instagram-new.png" alt="Instagram">
        </a>
      </div>
      <div>
        <a href="#">
          <img src="https://img.icons8.com/office/30/FF0000/twitter.png" alt="Twitter">
        </a>
      </div>
    </div>
  </div>
</header>
<div class="hub-card">
  <h1>Welcome To The Future !</h1>
  <p>Hey folks, welcome to Collabor8! Think of us as your friendly neighborhood hub. Here, we bring together local businesses and the community, allowing both to grow and succeed.</p>
  <div class="dropdown-container">
    <div class="dropdown">
      <select>
        <option value="">Find A Local Business</option>
        <option value="astronaut">Chippy</option>
        <option value="engineer">Window Cleaner</option>
        <option value="scientist">Hairdresser</option>
        <option value="pilot">RocketShip Parts</option>
      </select>
    </div>
  </div></div>
<div class="container">
    <div id="center-triangle" class="triangle"></div>
    <div id="left-triangle" class="triangle"></div>
    <div id="right-triangle" class="triangle"></div>
    <div class="reflect-container">
      <div class="reflect-text">F<span>o</span><span>r</span><span>d</span><span>i</span><span>e</span><span>s</span></div>
      <div class="reflection">P<span>r</span><span>e</span><span>s</span><span>s</span><span>M</span><span>e</span></div>
    </div>
    <a href="https://oavo33.github.io/WindowCleaning/" class="new-page-link" id="new-page-link">My Page</a>
  </div>
<div class="grid-container">
  <div class="grid-item community-item" onclick="window.location.href = 'https://oavo33.github.io/Elderly.assistance/';">
    <i class="community-icon">👵👴🏽</i>
    <p class="community-text">Elderly Assistance</p>
  </div>
  <div class="grid-item community-item" onclick="window.location.href = 'https://oavo33.github.io/Personalized.Exchange.And.Free.Services/';">
    <i class="community-icon">🤝</i>
    <p class="community-text">Community Giveaway</p>
  </div>
  <div class="grid-item community-item" onclick="window.location.href = 'https://oavo33.github.io/The.Community.Graffiti.Wall/';">
    <i class="community-icon">🎨</i>
    <p class="community-text">The Community Graffiti Wall</p>
  </div>
  <div class="grid-item community-item" onclick="window.location.href = 'https://oavo33.github.io/Vintage.High.Street/';">
    <i class="community-icon">📸</i>
    <p class="community-text">Our Vintage Shop Photographs</p>
  </div>
  <div class="grid-item community-item" onclick="window.location.href = 'https://oavo33.github.io/Help/';">
    <i class="community-icon">🏠</i>
    <p class="community-text">Help Our Homeless</p>
  </div>
  <div class="grid-item community-item" onclick="window.location.href = 'https://oavo33.github.io/The.Hub/';">
    <i class="community-icon">💼</i>
    <p class="community-text">Encouraging Young Entrepreneurship</p>
  </div>
  <div class="grid-item community-item" onclick="window.location.href = 'https://oavo33.github.io/Personalized.Web.Pages/'">
    <i class="community-icon">🌐</i>
    <p class="community-text">FREE Personalized Web Pages, Every Month</p>
  </div>
  <div class="grid-item community-item" onclick="window.location.href = 'https://oavo33.github.io/White.Paper/'">
    <i class="community-icon">📝</i>
    <p class="community-text">White Paper</p>
    <p class="hover-text">Want to Know how Our Community will flourish BY local business? Please read: Section 6.4, That's how our Community gets paid! The more we interact with Local Business, The more we get Paid by Them, Pop in say Thanks</p>
  </div>
</div>
<footer>
  <div class="footer-container">
    <div class="box" onclick="window.location.href = 'https://oavo33.github.io/GitHubz/';">
      <h3>What Do You Think About Our Community Hub?</h3>
    </div>
  </div>
  <div class="footer-container">
    <p>&copy; 2023 Lofties. All rights reserved.</p>
  </div>
</footer>
<script>
  const centerTriangle = document.getElementById('center-triangle');
  const leftTriangle = document.getElementById('left-triangle');
  const rightTriangle = document.getElementById('right-triangle');
  centerTriangle.addEventListener('mouseover', handleTriangleHover);
  centerTriangle.addEventListener('touchstart', handleTriangleHover);
  centerTriangle.addEventListener('mouseout', handleTriangleHover);
  centerTriangle.addEventListener('touchend', handleTriangleHover);
  function handleTriangleHover(event) {
    if (event.type === 'mouseover' || event.type === 'touchstart') {
      leftTriangle.style.transform = 'translate(-50%, -50%) translateX(46px) translateY(2px)';
      rightTriangle.style.transform = 'translate(-50%, -50%) translateX(46px) translateY(-58px)';
    } else if (event.type === 'mouseout' || event.type === 'touchend') {
      leftTriangle.style.transform = 'translate(-50%, -50%)';
      rightTriangle.style.transform = 'translate(-50%, -50%)';
    }
  }
  document.getElementById("new-page-link").addEventListener("click", function(event) {
      event.preventDefault();
      window.location.href = "https://oavo33.github.io/WindowCleaning/";
    });
</script>
</body>
</html>
