<template>
    <div class="course-materials-container">
      <div class="course-materials-content">
        <h1>Course Materials</h1>
        <table>
          <thead>
            <tr>
              <th>Title</th>
              <th>Description</th>
              <th>Download</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="material in courseMaterials" :key="material.id">
              <td>{{ material.title }}</td>
              <td>{{ material.description }}</td>
              <td><a :href="material.link" target="_blank">Download</a></td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: "CourseMaterialsPage",
    data() {
      return {
        courseMaterials: [
          {
            id: 1,
            title: "Lecture 1: Introduction to Web Technology",
            description: "An introduction to the fundamentals of web technology.",
            link: "path/to/lecture1.pdf",
          },
          {
            id: 2,
            title: "Lecture 2: HTML Basics",
            description: "A comprehensive guide to HTML basics.",
            link: "path/to/lecture2.pdf",
          },
          {
            id: 3,
            title: "Lecture 3: CSS Basics",
            description: "An overview of CSS for styling web pages.",
            link: "path/to/lecture3.pdf",
          },
          // Add more course materials as needed
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .course-materials-container {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px;
  }
  
  .course-materials-content {
    width: 800px;
    text-align: center;
  }
  
  .course-materials-content h1 {
    font-family: "Times New Roman", Times, serif;
    font-size: 36px;
    margin-bottom: 20px;
    color:#ff7200;
;
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
  