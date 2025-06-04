<script>
  let menuOpen = false;
</script>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    html, body {
      margin: 0; padding: 0; box-sizing: border-box;
      width: 100%; height: 100%;
    }
   
    .navbar {
      position: fixed;
      top: 0; left: 0; right: 0;
      height: 60px;
      background-color: #333;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 20px;
      margin: 0;
      box-sizing: border-box;
      z-index: 1000;
      color: white;
    }
  </style>
</head>
<body>

  <nav class="navbar">
    <div class="logo">MyApp</div>
    <button class="menu-toggle">☰</button>
    <ul>
      <li><a href="/" style="color:white;">Home</a></li>
      <li><a href="/about" style="color:white;">About</a></li>
      <li><a href="/services" style="color:white;">Services</a></li>
      <li><a href="/contact" style="color:white;">Contact</a></li>
    </ul>
  </nav>
</body>
</html>


<style>
/* Remove all default margin and padding */
html, body {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  width: 100%;
  height: 100%;
}

  .navbar {
  position: fixed; /* or fixed if you want sticky */
  background-color: #black;
  color: white;
  width: 100%;         /* full viewport width */
  margin: 0;           /* no auto-centering */
  padding: 0 20px;     /* optional side padding */
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 60px;        /* fixed height */
  box-sizing: border-box;
  z-index: 1000;       /* ensures navbar is on top */
}

  .logo {
    font-size: 1.5rem;
  }

  ul {
    list-style: none;
    display: flex;
    gap: 1.5rem;
  }

  li a {
    text-decoration: none;
    color: white;
    font-weight: bold;
  }

  .menu-toggle {
    display: none;
    font-size: 2rem;
    background: none;
    border: none;
    color: white;
    cursor: pointer;
  }

  @media (max-width: 768px) {
    ul {
      display: none;
      flex-direction: column;
      position: absolute;
      top: 0;
      right: 0;
      background-color: #black;
      padding: 1rem;
    }



 

    .menu-toggle {
      display: block;
    }
  }
</style>
