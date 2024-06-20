<template>
    <div class="assessment-container">
      <div class="assessment-content">
        <h1>Assessments</h1>
        <table>
          <thead>
            <tr>
              <th>Title</th>
              <th>Description</th>
              <th>Due Date</th>
              <th>Submit</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="assessment in assessments" :key="assessment.id">
              <td>{{ assessment.title }}</td>
              <td>{{ assessment.description }}</td>
              <td>{{ assessment.dueDate }}</td>
              <td><a :href="assessment.submitLink" target="_blank">Submit</a></td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "AssessmentPage",
    data() {
      return {
        assessments: [
          {
            id: 1,
            title: "Assignment 1: HTML Basics",
            description: "Create a simple HTML page with the given specifications.",
            dueDate: "2024-07-01",
            submitLink: "path/to/submit1",
          },
          {
            id: 2,
            title: "Quiz 1: CSS Basics",
            description: "Complete the quiz on CSS basics.",
            dueDate: "2024-07-05",
            submitLink: "path/to/submit2",
          },
          {
            id: 3,
            title: "Project 1: Build a Personal Website",
            description: "Develop a personal website using HTML, CSS, and JavaScript.",
            dueDate: "2024-07-15",
            submitLink: "path/to/submit3",
          },
          // Add more assessments as needed
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .assessment-container {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
  }
  
  .assessment-content {
    width: 800px;
    text-align: center;
  }
  
  .assessment-content h1 {
    font-family: "Times New Roman", Times, serif;
    font-size: 36px;
    margin-bottom: 20px;
    color: #ff7200;
  }
  
  table {
    width: 100%;
    border-collapse: collapse;
    margin-bottom: 20px;
  }
  
  th, td {
    border: 1px solid #ddd;
    padding: 8px;
    text-align: left;
  }
  
  th {
    background-color: #ff7200;
    color: white;
    font-family: Arial, sans-serif;
  }
  
  td {
    color: white;
    font-family: Arial, sans-serif;
  }
  
  a {
    color: #ff7200;
    text-decoration: none;
  }
  
  a:hover {
    text-decoration: underline;
  }
  </style>
  