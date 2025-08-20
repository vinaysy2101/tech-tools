# tech-tools
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Vinay's Tech Toolbox</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f4f4f4;
      color: #333;
      transition: background-color 0.3s, color 0.3s;
    }
    header {
      background-color: #0078D7;
      color: white;
      padding: 1rem;
      text-align: center;
    }
    .container {
      padding: 2rem;
    }
    .section {
      margin-bottom: 1.5rem;
    }
    details {
      background: #e0e0e0;
      padding: 1rem;
      border-radius: 8px;
    }
    summary {
      font-weight: bold;
      cursor: pointer;
    }
    .toggle-btn {
      margin-top: 1rem;
      padding: 0.5rem 1rem;
      background-color: #0078D7;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .dark-mode {
      background-color: #1e1e1e;
      color: #f4f4f4;
    }
    .dark-mode details {
      background-color: #333;
    }
    pre {
      background-color: #222;
      color: #0f0;
      padding: 1rem;
      border-radius: 8px;
      overflow-x: auto;
    }
    input, button {
      margin-top: 0.5rem;
      padding: 0.5rem;
      border-radius: 5px;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>
  <header>
    <h1>Vinay's Tech Toolbox 🧠</h1>
    <p>Explore my favorite tools, languages, games, and troubleshooting tricks</p>
  </header>

  <div class="container">

    <!-- Programming Languages -->
    <div class="section">
      <details>
        <summary>💻 Programming Languages</summary>
        <ul>
          <li>Java – OOP, GUI apps</li>
          <li>Python – Games with Pygame</li>
          <li>C – Low-level logic</li>
        </ul>
      </details>
    </div>

    <!-- System Tweaks -->
    <div class="section">
      <details>
        <summary>🛠️ System Tweaks</summary>
        <ul>
          <li>BIOS settings for boot issues</li>
          <li>Windows Registry hacks</li>
          <li>Safe Mode troubleshooting</li>
        </ul>
      </details>
    </div>

    <!-- Web Projects -->
    <div class="section">
      <details>
        <summary>🌐 Web Projects</summary>
        <ul>
          <li>HTML + CSS portfolio</li>
          <li>Live Server setup</li>
          <li>Domain registration tips</li>
        </ul>
      </details>
    </div>

    <!-- Click Counter Game -->
    <div class="section">
      <details>
        <summary>🎯 Click Counter Game</summary>
        <p>Click as fast as you can!</p>
        <button onclick="countClicks()">Click Me!</button>
        <p id="clicks">Clicks: 0</p>
      </details>
    </div>

    <!-- Guess the Number Game -->
    <div class="section">
      <details>
        <summary>🔢 Guess the Number</summary>
        <p>Guess a number between 1 and 10:</p>
        <input type="number" id="guess" />
        <button onclick="checkGuess()">Submit</button>
        <p id="result"></p>
      </details>
    </div>

    <!-- C Code -->
    <div class="section">
      <details>
        <summary>🧮 C Code: Calculator</summary>
        <pre><code>
#include &lt;stdio.h&gt;

int main() {
  int a, b;
  char op;
  printf("Enter expression (e.g. 3 + 2): ");
  scanf("%d %c %d", &a, &op, &b);
  switch(op) {
    case '+': printf("%d\n", a + b); break;
    case '-': printf("%d\n", a - b); break;
    case '*': printf("%d\n", a * b); break;
    case '/': printf("%d\n", a / b); break;
    default: printf("Invalid operator\n");
  }
  return 0;
}
        </code></pre>
      </details>
    </div>

    <!-- Python Code -->
    <div class="section">
      <details>
        <summary>🐦 Python: Flappy Bird Snippet</summary>
        <pre><code>
import pygame
pygame.init()
win = pygame.display.set_mode((500, 500))
bird_y = 250
gravity = 0.5
while True:
  bird_y += gravity
  win.fill((255, 255, 255))
  pygame.draw.circle(win, (255, 0, 0), (250, int(bird_y)), 20)
  pygame.display.update()
        </code></pre>
      </details>
    </div>

    <!-- Java Code -->
    <div class="section">
      <details>
        <summary>✅ Java: Input Validation</summary>
        <pre><code>
import java.util.Scanner;

public class ValidateInput {
  public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    System.out.print("Enter a number: ");
    if (sc.hasNextInt()) {
      int num = sc.nextInt();
      System.out.println("You entered: " + num);
    } else {
      System.out.println("Invalid input!");
    }
  }
}
        </code></pre>
      </details>
    </div>

    <!-- Dark Mode Toggle -->
    <button class="toggle-btn" onclick="toggleDarkMode()">Toggle Dark Mode 🌙</button>
  </div>

  <script>
    let clicks = 0;
    function countClicks() {
      clicks++;
      document.getElementById("clicks").innerText = "Clicks: " + clicks;
    }

    const number = Math.floor(Math.random() * 10) + 1;
    function checkGuess() {
      const guess = parseInt(document.getElementById("guess").value);
      const result = document.getElementById("result");
      result.innerText = guess === number ? "Correct!" : "Try again!";
    }

    function toggleDarkMode() {
      document.body.classList.toggle('dark-mode');
    }
  </script>
</body>
</html>
