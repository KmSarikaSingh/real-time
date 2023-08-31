# real-time
This is  real-time character counter that counts the number of characters in a textarea and displays the total number of characters in the textbox and the number of remaining characters in the textbox.

# Hosted Link- https://kmsarikasingh.github.io/real-time/

# HTML
This is HTML code creates a simple webpage with a textarea and two paragraphs those display the total number of characters and the number of remaining characters in the textbox.
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Real-time Charater Counter</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="container">
      <h2>Real-time Charater Counter</h2>
      <textarea id="textarea" class="textarea" placeholder="Please write your text here..." maxlength="50"
      ></textarea>
      <div class="counter">
        <p>
          Total Charaters:
          <span class="total-counter" id="total-counter"></span>
        </p>
        <p>
          Remaining:
          <span class="remaining-counter" id="remaining-counter"></span>
        </p>
      </div>
    </div>
    <script src="index.js"></script>
  </body>
</html>
```
# CSS
it's code provide the styles of textarea and the counter container.
```
body {
    margin: 0;
    display: flex;
    justify-content: center;
    height: 100vh;
    align-items: center;
    background-color: salmon;
  }
  
  .container {
    background-color: lightpink;
    width: 400px;
    padding: 20px;
    margin: 5px;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
  }
  
  .textarea {
    resize: none;
    width: 100%;
    height: 100px;
    font-size: 18px;
    font-family: sans-serif;
    padding: 10px;
    box-sizing: border-box;
    border: solid 2px darkgray;
  }
  
  .counter {
    display: flex;
    justify-content: space-between;
    padding: 0 5px;
  }
  
  .counter p {
    font-size: 18px;
    font-family: cursive;
    color: rgb(109, 104, 104);
  }
  
  .total-counter {
    color: slateblue;
  }
  
  .remaining-counter {
    color: orangered;
  }
  ```
# JAVASCRIPT
```
const textareaEl = document.getElementById("textarea");
const totalCounterEl = document.getElementById("total-counter");
const remainingCounterEl = document.getElementById("remaining-counter");

textareaEl.addEventListener("keyup", () => {
  updateCounter();
});

updateCounter()

function updateCounter() {
  totalCounterEl.innerText = textareaEl.value.length;
  remainingCounterEl.innerText =
    textareaEl.getAttribute("maxLength") - textareaEl.value.length;
}
```
