# PRODIGY_TrackCode_task1
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Navigation Menu</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="menu" id="menu">
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </div>
  <div class="content">
    <!-- Your website content goes here -->
  </div>
  <script src="script.js"></script>
</body>
</html>
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

.menu {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: #333;
  padding: 10px 0;
  z-index: 1000;
}

.menu ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  text-align: center;
}

.menu ul li {
  display: inline-block;
  margin-right: 20px;
}

.menu ul li a {
  color: #fff;
  text-decoration: none;
  padding: 10px;
}

.menu ul li a:hover {
  background-color: #555;
}

.scrolled {
  background-color: #222;
}

.hovered {
  color: #ff8c00;
}
window.addEventListener('scroll', function() {
  const menu = document.getElementById('menu');
  if (window.scrollY > 50) {
    menu.classList.add('scrolled');
  } else {
    menu.classList.remove('scrolled');
  }
});

const menuItems = document.querySelectorAll('.menu ul li a');
menuItems.forEach(item => {
  item.addEventListener('mouseenter', function() {
    this.classList.add('hovered');
  });
  item.addEventListener('mouseleave', function() {
    this.classList.remove('hovered');
  });
});

  

