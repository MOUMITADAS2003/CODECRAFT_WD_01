# CODECRAFT_WD_01
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Navigation Menu</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <nav id="navbar">
        <ul>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="home">
        <h1>Welcome to My Website</h1>
    </section>
    <section id="about">
        <h2>About Us</h2>
        <p>Some details about our company.</p>
    </section>
    <section id="services">
        <h2>Our Services</h2>
        <p>Details about services offered.</p>
    </section>
    <section id="contact">
        <h2>Contact Us</h2>
        <p>Reach out to us anytime.</p>
    </section>

    <script src="script.js"></script>
</body>
</html>

/* Basic styling */
body {
    margin: 0;
    font-family: Arial, sans-serif;
}

/* Fixed navigation bar */
nav {
    position: fixed;
    top: 0;
    width: 100%;
    background: rgba(0, 0, 0, 0.7); /* Transparent black */
    padding: 10px 0;
    transition: background 0.3s;
}

/* Style for navbar when scrolled */
nav.scrolled {
    background: #333; /* Darker background when scrolled */
}

/* Centering the nav items */
nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
}

nav ul li {
    margin: 0 20px;
}

nav ul li a {
    text-decoration: none;
    color: white;
    font-size: 18px;
    padding: 10px;
    transition: color 0.3s, background 0.3s;
}

/* Hover effect */
nav ul li a:hover {
    background: white;
    color: black;
    border-radius: 5px;
}

/* Section styling */
section {
    height: 100vh;
    padding: 20px;
    text-align: center;
}

#home { background: lightblue; }
#about { background: lightcoral; }
#services { background: lightgreen; }
#contact { background: lightsalmon; }

// Select the navigation bar
const navbar = document.getElementById("navbar");

// Add an event listener to change navbar background on scroll
window.addEventListener("scroll", () => {
    if (window.scrollY > 50) {
        navbar.classList.add("scrolled");
    } else {
        navbar.classList.remove("scrolled");
    }
});
