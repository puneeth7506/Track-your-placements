# Track-your-placements
Punith Klu, [05-11-2025 11:18 AM]
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Track Your Placements</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0; padding: 0;
      background: #f5f6fa;
      color: #333;
    }
    header {
      background: #00529b;
      color: white;
      padding: 1rem;
      text-align: center;
    }
    nav {
      display: flex;
      justify-content: center;
      background: #007acc;
    }
    nav button {
      background: #007acc;
      color: white;
      border: none;
      padding: 0.75rem 1.5rem;
      cursor: pointer;
      font-size: 1rem;
      transition: background 0.3s ease;
    }
    nav button:hover, nav button.active {
      background: #00529b;
    }
    main {
      padding: 2rem;
      max-width: 900px;
      margin: auto;
      background: white;
      box-shadow: 0 0 12px rgba(0,0,0,0.1);
      border-radius: 6px;
    }
    section {
      display: none;
    }
    section.active {
      display: block;
    }
    h2 {
      border-bottom: 2px solid #007acc;
      padding-bottom: 0.5rem;
    }
    label {
      display: block;
      margin-top: 1rem;
      font-weight: bold;
    }
    input[type="text"], input[type="email"], select, textarea {
      width: 100%;
      padding: 0.5rem;
      margin-top: 0.3rem;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
    button.submit-btn {
      margin-top: 1.5rem;
      padding: 0.75rem 1.5rem;
      background: #007acc;
      border: none;
      color: white;
      border-radius: 4px;
      cursor: pointer;
    }
    button.submit-btn:hover {
      background: #00529b;
    }
    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 1rem;
    }
    th, td {
      border: 1px solid #ccc;
      padding: 0.75rem;
      text-align: left;
    }
    th {
      background: #007acc;
      color: white;
    }
  </style>
</head>
<body>

<header>
  <h1>Track Your Placements</h1>
  <p>Streamline your placement journey: students, employers, officers, and admins</p>
</header>

<nav>
  <button class="tab-btn active" data-tab="student">Student</button>
  <button class="tab-btn" data-tab="employer">Employer</button>
  <button class="tab-btn" data-tab="officer">Placement Officer</button>
  <button class="tab-btn" data-tab="admin">Admin</button>
</nav>

<main>
  <!-- Student Section -->
  <section id="student" class="active">
    <h2>Student Dashboard</h2>
    <h3>Explore Job Opportunities</h3>
    <input type="text" placeholder="Search jobs by title or company..." />
    <button class="submit-btn">Search</button>

    <h3>Your Applications</h3>
    <table>
      <thead>
        <tr><th>Job Title</th><th>Company</th><th>Status</th></tr>
      </thead>
      <tbody>
        <tr><td>Software Engineer</td><td>ABC Tech</td><td>Under Review</td></tr>
        <tr><td>Data Analyst</td><td>XYZ Analytics</td><td>Interview Scheduled</td></tr>
      </tbody>
    </table>
  </section>

  <!-- Employer Section -->
  <section id="employer">
    <h2>Employer Dashboard</h2>
    <h3>Post a New Job</h3>
    <form>
      <label for="job-title">Job Title</label>
      <input type="text" id="job-title" name="job-title" required />

      <label for="company-name">Company Name</label>
      <input type="text" id="company-name" name="company-name" required />

      <label for="job-description">Job Description</label>
      <textarea id="job-description" name="job-description" rows="4" required></textarea>

      <button type="submit" class="submit-btn">Post Job</button>
    </form>

    <h3>Applications Received</h3>
    <table>
      <thead>
        <tr><th>Applicant Name</th><th>Job</th><th>Status</th></tr>
      </thead>
      <tbody>
        <tr><td>Jane Doe</td><td>Software Engineer</td><td>Pending Review</td></tr>
        <tr><td>John Smith</td><td>Data Analyst</td><td>Selected for Interview</td></tr>
      </tbody>
    </table>
  </section>

Punith Klu, [05-11-2025 11:18 AM]
<!-- Placement Officer Section -->
  <section id="officer">
    <h2>Placement Officer Dashboard</h2>
    <h3>Placement Records</h3>
    <table>
      <thead>
        <tr><th>Student Name</th><th>Job Title</th><th>Status</th></tr>
      </thead>
      <tbody>
        <tr><td>Alice Johnson</td><td>Product Manager</td><td>Placed</td></tr>
        <tr><td>Bob Brown</td><td>Marketing Analyst</td><td>Applied</td></tr>
      </tbody>
    </table>

    <h3>Generate Reports</h3>
    <button class="submit-btn">Download Placement Report</button>
  </section>

  <!-- Admin Section -->
  <section id="admin">
    <h2>Admin Dashboard</h2>
    <h3>Manage Users & Roles</h3>
    <form>
      <label for="user-email">User Email</label>
      <input type="email" id="user-email" name="user-email" required />

      <label for="user-role">Role</label>
      <select id="user-role" name="user-role" required>
        <option value="">Select Role</option>
        <option value="student">Student</option>
        <option value="employer">Employer</option>
        <option value="officer">Placement Officer</option>
        <option value="admin">Admin</option>
      </select>

      <button type="submit" class="submit-btn">Update Role</button>
    </form>

    <h3>System Settings</h3>
    <button class="submit-btn">Manage System Configuration</button>
  </section>
</main>

<script>
  // Tab navigation logic
  const tabs = document.querySelectorAll('.tab-btn');
  const sections = document.querySelectorAll('main section');

  tabs.forEach(tab => {
    tab.addEventListener('click', () => {
      tabs.forEach(t => t.classList.remove('active'));
      tab.classList.add('active');

      const target = tab.getAttribute('data-tab');
      sections.forEach(section => {
        if(section.id === target) {
          section.classList.add('active');
        } else {
          section.classList.remove('active');
        }
      });
    });
  });
</script>

</body>
</html>
