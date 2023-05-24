# Student-Marks-Calculator-using-Html
<html><head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    .container {
      width: 500px;
      margin: 0 auto;
      text-align: center;
    }
    
    input[type="number"] {
      width: 50px;
      height: 25px;
      margin-bottom: 20px;
    }
    
    button[type="submit"] {
      background-color: lightblue;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Marks Card Generator</h1>
    <form id="marks-form">
      <label for="subject1">Subject 1:</label>
      <input type="number" id="subject1" name="subject1">
      <label for="subject2">Subject 2:</label>
      <input type="number" id="subject2" name="subject2">
      <label for="subject3">Subject 3:</label>
      <input type="number" id="subject3" name="subject3">
      <button type="submit">Submit</button>
    </form>
    <p id="result"></p>
  </div>
  <script>
    const form = document.querySelector("#marks-form");
const result = document.querySelector("#result");

form.addEventListener("submit", (e) => {
  e.preventDefault();
  const subject1 = form.subject1.value;
  const subject2 = form.subject2.value;
  const subject3 = form.subject3.value;
  const average = (parseInt(subject1) + parseInt(subject2) + parseInt(subject3)) / 3;
  result.textContent = `Average: ${average}`;
});
</script>

</body></html>
