<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Days Lived Calculator</title>
</head>
<body>

<h1>Days Lived Calculator</h1>

<form id="birthdateForm">
  <label for="birthdate">Enter Your Birthdate:</label>
  <input type="date" id="birthdate" name="birthdate">
  <button type="submit">Calculate</button>
</form>

<div id="result"></div>

<script>
document.getElementById('birthdateForm').addEventListener('submit', function(event) {
  event.preventDefault(); // Prevent form submission
  
  // Get user's birthdate from the input field
  const birthdate = new Date(document.getElementById('birthdate').value);
  
  // Calculate the number of days lived
  const currentDate = new Date();
  const daysLived = Math.floor((currentDate - birthdate) / (1000 * 60 * 60 * 24));
  
  // Display the result on the webpage
  document.getElementById('result').textContent = `You have lived approximately ${daysLived} days on Earth.`;
});
</script>

</body>
</html>
