<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bright Future School</title>

  <style>
    /* Basic reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, sans-serif;
    }

    body {
      background-color: #f4f8ff;
      color: #222;
      line-height: 1.6;
    }

    /* Header section */
    header {
      background: #0b5ed7;
      color: white;
      padding: 15px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
    }

    header h1 {
      font-size: 24px;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 20px;
      font-weight: bold;
      transition: 0.3s;
    }

    nav a:hover {
      color: #ffd700;
    }

    /* Home section */
    .home {
      background: linear-gradient(rgba(0, 80, 180, 0.6), rgba(0, 80, 180, 0.6)),
      url("https://images.unsplash.com/photo-1580582932707-520aed937b7b?auto=format&fit=crop&w=1200&q=80");
      background-size: cover;
      background-position: center;
      color: white;
      text-align: center;
      padding: 100px 20px;
    }

    .home h2 {
      font-size: 42px;
      margin-bottom: 15px;
    }

    .home p {
      font-size: 18px;
      margin-bottom: 25px;
    }

    button {
      background: #ffd700;
      color: #222;
      border: none;
      padding: 12px 22px;
      border-radius: 25px;
      cursor: pointer;
      font-weight: bold;
      transition: 0.3s;
    }

    button:hover {
      background: white;
      transform: scale(1.05);
    }

    /* Common section styling */
    section {
      padding: 60px 40px;
      text-align: center;
    }

    section h2 {
      color: #0b5ed7;
      margin-bottom: 20px;
      font-size: 30px;
    }

    /* About section */
    .about p {
      max-width: 750px;
      margin: auto;
      font-size: 17px;
    }

    /* Courses section */
    .course-container {
      display: flex;
      justify-content: center;
      gap: 25px;
      flex-wrap: wrap;
      margin-top: 30px;
    }

    .course-card {
      background: white;
      width: 280px;
      padding: 25px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
      transition: 0.3s;
    }

    .course-card:hover {
      transform: translateY(-8px);
    }

    .course-card h3 {
      color: #0b5ed7;
      margin-bottom: 10px;
    }

    /* Contact form */
    form {
      max-width: 450px;
      margin: auto;
      background: white;
      padding: 25px;
      border-radius: 12px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
    }

    input, textarea {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 15px;
    }

    textarea {
      resize: none;
      height: 100px;
    }

    .message {
      margin-top: 15px;
      color: green;
      font-weight: bold;
    }

    /* Footer */
    footer {
      background: #0b5ed7;
      color: white;
      text-align: center;
      padding: 15px;
    }

    /* Responsive design for mobile */
    @media (max-width: 768px) {
      header {
        flex-direction: column;
        text-align: center;
      }

      nav {
        margin-top: 10px;
      }

      nav a {
        display: inline-block;
        margin: 8px;
      }

      .home h2 {
        font-size: 30px;
      }

      section {
        padding: 40px 20px;
      }
    }
  </style>
</head>

<body>

  <!-- Header with school name and navigation -->
  <header>
    <h1>Bright Future School</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#courses">Courses</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- Home section with banner image -->
  <section class="home" id="home">
    <h2>Welcome to Bright Future School</h2>
    <p>Learning today, leading tomorrow.</p>
    <button onclick="showWelcome()">Click for Welcome Message</button>
    <p class="message" id="welcomeText"></p>
  </section>

  <!-- About section -->
  <section class="about" id="about">
    <h2>About Our School</h2>
    <p>
      Bright Future School provides quality education with modern teaching methods.
      Our aim is to develop students academically, socially, and creatively.
      We focus on discipline, confidence, and practical learning.
    </p>
  </section>

  <!-- Courses section -->
  <section class="courses" id="courses">
    <h2>Our Courses</h2>

    <div class="course-container">
      <div class="course-card">
        <h3>Science</h3>
        <p>Learn physics, chemistry, biology, and practical experiments.</p>
      </div>

      <div class="course-card">
        <h3>Mathematics</h3>
        <p>Improve problem-solving skills with basic and advanced maths.</p>
      </div>

      <div class="course-card">
        <h3>Computer Studies</h3>
        <p>Learn computer basics, coding, internet, and digital skills.</p>
      </div>
    </div>
  </section>

  <!-- Contact section with form -->
  <section class="contact" id="contact">
    <h2>Contact Us</h2>

    <form onsubmit="return validateForm()">
      <input type="text" id="name" placeholder="Enter your name">
      <input type="email" id="email" placeholder="Enter your email">
      <textarea id="message" placeholder="Enter your message"></textarea>
      <button type="submit">Submit</button>
    </form>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2026 Bright Future School. All Rights Reserved.</p>
  </footer>

  <script>
    // Function to show welcome message
    function showWelcome() {
      document.getElementById("welcomeText").innerHTML = "Welcome to our school!";
    }

    // Function to validate contact form
    function validateForm() {
      let name = document.getElementById("name").value.trim();
      let email = document.getElementById("email").value.trim();
      let message = document.getElementById("message").value.trim();

      // Simple email format check
      let emailPattern = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/;

      // Check empty fields
      if (name === "" || email === "" || message === "") {
        alert("Please fill all fields.");
        return false;
      }

      // Check valid email
      if (!email.match(emailPattern)) {
        alert("Please enter a valid email address.");
        return false;
      }

      // Success message
      alert("Thank you! Your message has been submitted successfully.");

      // Clear form fields
      document.getElementById("name").value = "";
      document.getElementById("email").value = "";
      document.getElementById("message").value = "";

      return false;
    }
  </script>

</body>
</html>
