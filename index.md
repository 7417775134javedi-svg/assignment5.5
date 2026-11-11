Here is the complete solution for your CSS Fundamentals Mini-Project assignment. It includes a multi-page college club website design with clean, reusable external CSS, a consistent color palette, styled navigation, buttons, forms, tables, and the required design choice explanation.

1. The Design Stylesheet (style.css)
Save this file as style.css. It incorporates CSS variables, typography, and clean layout styles for your pages.

CSS
/* ==========================================
   1. Design Tokens & Variables
   ================================---------- */
:root {
  --color-primary: #1e3a8a;      /* Deep Navy Blue */
  --color-primary-dark: #1e293b; /* Dark Slate for footers/accents */
  --color-accent: #f59e0b;       /* Warm Gold/Amber for CTAs */
  --color-background: #f8fafc;   /* Light background */
  --color-surface: #ffffff;      /* White card/container background */
  --color-text: #334155;         /* Dark neutral body text */
  --color-text-heading: #0f172a; /* Near-black for headings */
  --color-border: #cbd5e1;       /* Subtle border color */

  --space-sm: 0.5rem;
  --space-md: 1rem;
  --space-lg: 2rem;

  --font-sans: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --radius: 6px;
  --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
}

/* ==========================================
   2. Global & Typography Styles
   ================================---------- */
* {
  box-sizing: border-box;
}

body {
  font-family: var(--font-sans);
  background-color: var(--color-background);
  color: var(--color-text);
  margin: 0;
  line-height: 1.6;
}

h1, h2, h3, h4 {
  color: var(--color-text-heading);
  margin-top: 0;
}

p {
  margin-bottom: var(--space-md);
}

/* ==========================================
   3. Navigation Bar
   ================================---------- */
header {
  background-color: var(--color-primary);
  color: #ffffff;
  padding: var(--space-md) var(--space-lg);
  box-shadow: var(--shadow);
}

.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1100px;
  margin: 0 auto;
}

.logo {
  font-size: 1.25rem;
  font-weight: bold;
  color: #ffffff;
  text-decoration: none;
}

nav ul {
  list-style: none;
  display: flex;
  gap: var(--space-lg);
  margin: 0;
  padding: 0;
}

nav a {
  color: #e2e8f0;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.2s ease;
}

nav a:hover, nav a.active {
  color: var(--color-accent);
}

/* ==========================================
   4. Layout & Content Containers
   ================================---------- */
main {
  max-width: 1100px;
  margin: var(--space-lg) auto;
  padding: 0 var(--space-lg);
}

.card {
  background-color: var(--color-surface);
  padding: var(--space-lg);
  border-radius: var(--radius);
  box-shadow: var(--shadow);
  margin-bottom: var(--space-lg);
  border-left: 4px solid var(--color-primary);
}

/* ==========================================
   5. Buttons & Interactive Elements
   ================================---------- */
.btn {
  display: inline-block;
  background-color: var(--color-accent);
  color: var(--color-primary-dark);
  padding: 0.6rem 1.2rem;
  font-weight: 600;
  text-decoration: none;
  border: none;
  border-radius: var(--radius);
  cursor: pointer;
  transition: opacity 0.2s ease;
}

.btn:hover {
  opacity: 0.9;
}

/* ==========================================
   6. Tables (Events / Schedule)
   ================================---------- */
.table-container {
  overflow-x: auto;
  margin-bottom: var(--space-lg);
}

table {
  width: 100%;
  border-collapse: collapse;
  background-color: var(--color-surface);
  border-radius: var(--radius);
  overflow: hidden;
  box-shadow: var(--shadow);
}

th, td {
  padding: var(--space-md);
  text-align: left;
  border-bottom: 1px solid var(--color-border);
}

th {
  background-color: var(--color-primary);
  color: #ffffff;
  font-weight: 600;
}

tr:hover {
  background-color: #f1f5f9;
}

/* ==========================================
   7. Forms (Membership / Contact)
   ================================---------- */
form {
  background-color: var(--color-surface);
  padding: var(--space-lg);
  border-radius: var(--radius);
  box-shadow: var(--shadow);
  max-width: 600px;
}

.form-group {
  margin-bottom: var(--space-md);
}

label {
  display: block;
  font-weight: 600;
  margin-bottom: var(--space-sm);
  color: var(--color-text-heading);
}

input[type="text"],
input[type="email"],
select,
textarea {
  width: 100%;
  padding: 0.75rem;
  border: 1px solid var(--color-border);
  border-radius: var(--radius);
  font-size: 1rem;
  font-family: var(--font-sans);
}

input:focus, select:focus, textarea:focus {
  outline: none;
  border-color: var(--color-primary);
  box-shadow: 0 0 0 3px rgba(30, 58, 138, 0.15);
}

/* ==========================================
   8. Footer
   ================================---------- */
footer {
  background-color: var(--color-primary-dark);
  color: #94a3b8;
  text-align: center;
  padding: var(--space-lg);
  margin-top: var(--space-lg);
  font-size: 0.9rem;
}
2. Sample Webpage 1: Home (index.html)
Save this as index.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TechCraft Club - Home</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <div class="nav-container">
      <a href="index.html" class="logo">💻 TechCraft Club</a>
      <nav>
        <ul>
          <li><a href="index.html" class="active">Home</a></li>
          <li><a href="events.html">Events</a></li>
          <li><a href="join.html">Join Us</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>
    <section class="card">
      <h1>Welcome to TechCraft Club</h1>
      <p>We build, code, and learn together. Whether you are a seasoned developer or writing your very first line of HTML, our club is a space to grow your technical skills through hands-on projects.</p>
      <a href="join.html" class="btn">Become a Member</a>
    </section>
  </main>

  <footer>
    <p>&copy; 2026 TechCraft Club. All rights reserved.</p>
  </footer>
</body>
</html>
3. Sample Webpage 2: Events Schedule (events.html)
Save this as events.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TechCraft Club - Events</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <div class="nav-container">
      <a href="index.html" class="logo">💻 TechCraft Club</a>
      <nav>
        <ul>
          <li><a href="index.html">Home</a></li>
          <li><a href="events.html" class="active">Events</a></li>
          <li><a href="join.html">Join Us</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>
    <h2>Upcoming Club Events</h2>
    <div class="table-container">
      <table>
        <thead>
          <tr>
            <th>Event Name</th>
            <th>Date</th>
            <th>Location</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>Intro to Git & GitHub</td>
            <td>March 15, 2026</td>
            <td>Lab 302 / Online</td>
          </tr>
          <tr>
            <td>Hackathon 2026 Kickoff</td>
            <td>April 2, 2026</td>
            <td>Student Union Hall</td>
          </tr>
          <tr>
            <td>Web Design Showcase</td>
            <td>May 10, 2026</td>
            <td>Auditorium B</td>
          </tr>
        </tbody>
      </table>
    </div>
  </main>

  <footer>
    <p>&copy; 2026 TechCraft Club. All rights reserved.</p>
  </footer>
</body>
</html>
4. Sample Webpage 3: Membership Form (join.html)
Save this as join.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TechCraft Club - Join Us</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <div class="nav-container">
      <a href="index.html" class="logo">💻 TechCraft Club</a>
      <nav>
        <ul>
          <li><a href="index.html">Home</a></li>
          <li><a href="events.html">Events</a></li>
          <li><a href="join.html" class="active">Apply Here</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <main>
    <h2>Join TechCraft Club</h2>
    <form action="#" method="POST">
      <div class="form-group">
        <label for="fullname">Full Name</label>
        <input type="text" id="fullname" name="fullname" placeholder="Jane Doe" required>
      </div>

      <div class="form-group">
        <label for="email">Campus Email</label>
        <input type="email" id="email" name="email" placeholder="student@college.edu" required>
      </div>

      <div class="form-group">
        <label for="interest">Primary Interest Area</label>
        <select id="interest" name="interest">
          <option value="web">Web Development</option>
          <option value="ai">Artificial Intelligence</option>
          <option value="cyber">Cybersecurity</option>
        </select>
      </div>

      <button type="submit" class="btn">Submit Application</button>
    </form>
  </main>

  <footer>
    <p>&copy; 2026 TechCraft Club. All rights reserved.</p>
  </footer>
</body>
</html>
5. Explanation of Design Choices (Submission Requirement)
Copy and paste this 4–5 line section into your assignment write-up:

We selected a deep navy blue primary color combined with a warm gold accent to establish a professional yet energetic brand identity suitable for a technology club. A clean sans-serif system font stack ensures high readability across all devices. The layout relies on CSS variables and modular cards to maintain consistency, while tables and forms incorporate clear padding, borders, and interactive focus states for optimal user experience.