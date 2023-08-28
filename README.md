<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>JS For Beginners</title>
    <!-- <link rel="stylesheet" href="style.css" /> -->
    <style>
      body {
        font-family: Arial, Helvetica, sans-serif;
        line-height: 1.6;
      }

      ul {
        list-style: none;
      }

      ul li {
        padding: 5px;
        background: #f4f4f4;
        margin: 5px 0;
      }

      header {
        background: #f4f4f4;
        padding: 1rem;
        text-align: center;
      }

      .container {
        margin: auto;
        width: 500px;
        overflow: auto;
        padding: 3rem 2rem;
      }

      #my-form {
        padding: 2rem;
        background: #f4f4f4;
      }

      #my-form label {
        display: block;
      }

      #my-form input[type="text"] {
        width: 100%;
        padding: 8px;
        margin-bottom: 10px;
        border-radius: 5px;
        border: 1px solid #ccc;
      }

      .btn {
        display: block;
        width: 100%;
        padding: 10px 15px;
        border: 0;
        background: #333;
        color: #fff;
        border-radius: 5px;
        margin: 5px 0;
      }

      .btn:hover {
        background: #444;
      }

      .bg-dark {
        background: #333;
        color: #fff;
      }
    </style>
  </head>
  <body>
    <header>
      <h1>JS For Beginners</h1>
    </header>

    <section class="container">
      <form id="my-form">
        <h1>Add User</h1>
        <div class="msg"></div>
        <div>
          <label for="name">Name:</label>
          <input type="text" id="name" />
        </div>
        <div>
          <label for="email">Email:</label>
          <input type="text" id="email" />
        </div>
        <input class="btn" type="submit" value="Submit" />
      </form>

      <!-- <ul id="users"></ul>
      <ul class="items">
        <li class="item">Item 1</li>
        <li class="item">Item 2</li>
        <li class="item">Item 3</li>
      </ul> -->
    </section>

    <script>
      let btn = document.querySelector(".btn");
      let name = document.querySelector("#name");
      let email = document.querySelector("#email");
      let form = document.querySelector("#my-form");
      let msg = document.querySelector(".msg");

      btn.addEventListener("click", (e) => {
        e.preventDefault();
        if (name.value === "" || email.value === "") {
          msg.innerHTML = "Plaese enter all field";
        } else {
          console.log("Form submitted");
          console.log(name.value, email.value);
        }
        console.log("button was clicked");
      });
      btn.addEventListener("mouseover", (e) => {
        e.preventDefault();
        console.log("mouse was hovered");
      });
      btn.addEventListener("mouseout", (e) => {
        e.preventDefault();
        console.log("mouse was out");
      });
    </script>
  </body>
</html>
