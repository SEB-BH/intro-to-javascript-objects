<h1>
  <span class="headline">Intro to JavaScript Objects</span>
  <span class="subhead">Setup</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to run a JavaScript file with Node.js and see its output.

We will build a small shopping cart in `app.js`. You can use one file for the whole lesson. When a section shows a new `const cart = ...` example, **replace** the previous version in your file rather than declaring `cart` twice.

Open a terminal and go to your lectures directory. If your course uses a different location, go there instead:

```bash
cd ~/code/ga/lectures
mkdir intro-to-javascript-objects
cd intro-to-javascript-objects
touch app.js
code .
```

On Windows, these commands work in Git Bash. You can also create the folder and file with VS Code.

Put this in `app.js` to check your setup:

```javascript
console.log('Shopping cart ready!');
```

In the same folder, run:

```bash
node app.js
```

You should see `Shopping cart ready!` in the terminal. If you do not, check that the terminal is inside the folder containing `app.js`.
