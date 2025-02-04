<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exercise 4 - Arrays</title>
</head>
<body>
  <div>
    <label for="a">a:</label>
    <input type="number" id="a" />

    <label for="b">b:</label>
    <input type="number" id="b" />

    <label for="l">l:</label>
    <input type="number" id="l" style="width: 300px;" />

    <button onclick="calculateSum()">Calculate Sum</button>
  </div>

  <script>
    function calculateSum() {
      // Get values from inputs
      const a = parseInt(document.getElementById('a').value);
      const b = parseInt(document.getElementById('b').value);
      const l = parseInt(document.getElementById('l').value);

      // Calculate sum of multiples of a or b up to l
      let sum = 0;
      for (let i = 1; i <= l; i++) {
        if (i % a === 0 || i % b === 0) {
          sum += i;
        }
      }

      // Alert the result
      alert(The sum of all multiples of ${a} or ${b} up to ${l} is: ${sum});
    }
  </script>
</body>
</html>
