<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gitam Dashboard</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }
    body {
      display: flex;
      min-height: 100vh;
      background-color: #f4f9f4;
    }
    .sidebar {
      width: 220px;
      background-color: #006400;
      color: white;
      padding: 20px;
    }
    .sidebar h2 {
      margin-bottom: 30px;
      font-size: 22px;
      text-align: center;
      border-bottom: 2px solid white;
      padding-bottom: 10px;
    }
    .sidebar ul {
      list-style: none;
    }
    .sidebar ul li {
      padding: 12px 10px;
      cursor: pointer;
      transition: 0.3s;
    }
    .sidebar ul li:hover {
      background-color: #004d00;
      border-radius: 5px;
    }
    .main {
      flex: 1;
      padding: 20px;
    }
    .header {
      background-color: #009900;
      color: white;
      padding: 15px;
      border-radius: 10px;
      font-size: 24px;
      font-weight: bold;
      margin-bottom: 20px;
    }
    .section {
      display: none;
    }
    .active {
      display: block;
    }
    .card, table {
      background: white;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      padding: 15px;
      margin-bottom: 20px;
    }
    table {
      width: 100%;
      border-collapse: collapse;
    }
    th, td {
      border: 1px solid #ccc;
      padding: 10px;
      text-align: center;
    }
    th {
      background-color: #228B22;
      color: white;
    }
    .branches img {
      width: 100px;
      height: auto;
      border-radius: 5px;
    }
    .progress {
      background: #ccc;
      border-radius: 10px;
      overflow: hidden;
      height: 20px;
      margin-top: 10px;
    }
    .progress-bar {
      height: 100%;
      background-color: green;
      width: 85%;
      color: white;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="sidebar">
    <h2>GITAM Dashboard</h2>
    <ul>
      <li onclick="showSection('dashboard')">Dashboard</li>
      <li onclick="showSection('attendance')">Attendance</li>
      <li onclick="showSection('assignments')">Assignments</li>
      <li onclick="showSection('grades')">Grades</li>
    </ul>
  </div>

  <div class="main">
    <div class="header">Welcome, Student</div>

    <!-- Dashboard Section -->
    <div class="section active" id="dashboard">
      <div class="card">
        <h3>Top College Rankings</h3>
        <ul>
          <li>GITAM Visakhapatnam - Rank 10</li>
          <li>GITAM Hyderabad - Rank 15</li>
          <li>GITAM Bengaluru - Rank 20</li>
        </ul>
      </div>
      <div class="card branches">
        <h3>Available Branches</h3>
        <p><img src="https://via.placeholder.com/100" alt="CSE"/> CSE</p>
        <p><img src="https://via.placeholder.com/100" alt="ECE"/> ECE</p>
        <p><img src="https://via.placeholder.com/100" alt="MECH"/> Mechanical</p>
      </div>
    </div>

    <!-- Attendance Section -->
    <div class="section" id="attendance">
      <div class="card">
        <h3>Today's Attendance</h3>
        <p>Present: 5 / 6 Lectures</p>
      </div>
      <div class="card">
        <h3>Semester Attendance</h3>
        <p>Overall: 85%</p>
        <div class="progress">
          <div class="progress-bar">85%</div>
        </div>
      </div>
    </div>

    <!-- Assignments Section -->
    <div class="section" id="assignments">
      <div class="card">
        <h3>Pending Assignments</h3>
        <ul>
          <li>Maths - Due: July 10</li>
          <li>Physics - Due: July 12</li>
          <li>CSE - Due: July 14</li>
        </ul>
        <p>Note: Upload before the due date!</p>
      </div>
    </div>

    <!-- Grades Section -->
    <div class="section" id="grades">
      <div class="card">
        <h3>Student Grades</h3>
        <table>
          <tr><th>Subject</th><th>Grade</th></tr>
          <tr><td>Maths</td><td>A</td></tr>
          <tr><td>Physics</td><td>B+</td></tr>
          <tr><td>CSE</td><td>A+</td></tr>
        </table>
      </div>
    </div>
  </div>

  <script>
    function showSection(sectionId) {
      document.querySelectorAll('.section').forEach(sec => sec.classList.remove('active'));
      document.getElementById(sectionId).classList.add('active');
    }
  </script>
</body>
</html>
