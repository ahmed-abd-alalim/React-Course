<h1 align="center">Session 4: Fourth Spark 🔥</h1>

![Session 4](./repository-assets/session-4.jpg "Session 4")

<!-- ![topics 4](./repository-assets/topics-4.jpg "topics 4") -->

<p align="center">In this section, you’ll learn how to use React libraries 📦 to enhance your projects. We'll cover how to install and integrate them 🔧, when to use them 🤔, and how they can help simplify your code ✨.</p>

---

### Session Topics

- **[React Libraries Usage](#react-libraries-usage)**

- **[Examples Of Libraries Used](#examples-of-libraries-used)**

  - [Bootstrap](#bootstrap)
  - [React Icons](#react-icons)
  - [lottiefiles](#lottiefiles)
  - [React Helmet](#react-helmet)

- **[💡 Client Task](#client-task)**

---

### React Libraries Usage

  <p>React Libraries Usage refers to the practice of integrating and utilizing third-party libraries specifically designed to enhance and extend the functionality of React applications. These libraries may offer solutions for UI components</p>

---

### Examples Of Libraries Used

1. #### Bootstrap

   Bootstrap is a popular CSS framework used to build responsive and mobile-first websites. In React, Bootstrap can be used to style components quickly and consistently by applying predefined classes.

   [Bootstrap page](https://getbootstrap.com/)

   - Install:
     ```bash
     npm i bootstrap@5.3.5
     ```
     ***
   - Import:

     ##### The import must be made in the root file `(main.jsx or index.jsx)`.

     ```bash
     // Bootstrap CSS
     import "bootstrap/dist/css/bootstrap.min.css";

     // Bootstrap Bundle JS
     import "bootstrap/dist/js/bootstrap.bundle.min.js";
     ```

---

2. #### React Icons

   React Icons is a popular library that provides a collection of icons from many icon sets (like Font Awesome, Material Design Icons, Feather, etc.) packaged as React components. It allows developers to easily add scalable and customizable icons to their React apps without needing to import entire icon fonts or SVG files manually.

   [React Icons page](https://react-icons.github.io/react-icons/)

   - Install:

     ```bash
     npm install react-icons --save
     ```

     ***

   - Usage:

     Just click on the icon and its import command will appear.

     ```bash
     import { FaReact } from "react-icons/fa";
     ```

     Insert this into the code.

     ```bash
     <FaReact />
     ```

---

3. #### lottiefiles

   LottieFiles is a platform that provides lightweight, scalable animations in JSON format, powered by Lottie, an open-source animation library by Airbnb. In React, Lottie animations are commonly used to add engaging UI animations without heavy file sizes or complex coding

   [lottiefiles page](https://lottiefiles.com/)

   - Install:

     ```bash
     npm install lottie-react
     ```

   ***

   - Import:

     ```bash
     import Lottie from "lottie-react";

     // Lottie animation
     import name-of-animation-file from "path-to-lottie-json-file";
     ```

   ***

   - Usage:

     ```bash
      <Lottie
      animationData={name-of-animation-file}
      loop={true}
      autoplay={true}
     />
     ```

4. #### React Helmet

   React Helmet is a library used to manage changes to the <head> section of your HTML document in React applications. It allows you to dynamically update the title, meta tags, and other elements of the <head> for each page or component, ensuring that SEO (Search Engine Optimization), social media sharing, and other page metadata are properly configured.

   [React Helmet page](https://www.npmjs.com/package/react-helmet-async)

   - Install:

     ```bash
     npm i react-helmet-async
     ```

   ***

   - Import:

     ```bash
     import { Helmet } from "react-helmet-async";
     ```

   ***

   - Usage:

     ```bash
     <Helmet>
        <title>{#}</title>
        <meta name="description" content={#} />
        <meta name="keywords" content={#} />
        <meta name="author" content={#} />
        <meta property="og:title" content={#} />
        <meta
          property="og:description"
          content={#}
        />
        <meta property="og:url" content={#} />
        <meta property="og:type" content={#} />
      </Helmet>
     ```

---

<a id="client-task"></a>

### 💡 Client Task

```bash
Optimize login component that gives users a warm
Client: Lena Harper, Product Manager at "TaskWave" a lightweight productivity platform for remote teams.

🎯 Project Brief:
Lena wants a simple and elegant login component that gives users a warm, personalized welcome upon signing in. This will be used on the prototype landing page for investor demos and onboarding tests.

📌 The function should:
1️⃣ Display a styled login form with username and password fields.
2️⃣ After submitting the form, the login box should disappear.
3️⃣ A friendly greeting like "Welcome back, [username] 👋" should instantly appear in its place.

📁 Resources
Not needed user provides input dynamically.
```

<!-- ### 💻 Solution

<details>
  <summary>Click on it after trying to solve it yourself 😉</summary>

```bash
import React, { useState } from 'react';

export default function TaskWaveLogin() {
  const [formData, setFormData] = useState({
    username: '',
    password: '',
  });
  const [isLoggedIn, setIsLoggedIn] = useState(false);

  const handleChange = (e) => {
    const { name, value } = e.target;
    setFormData(prev => ({
      ...prev,
      [name]: value
    }));
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    if (formData.username.trim()) {
      setIsLoggedIn(true);
    }
  };

  return (
    <div>
      {!isLoggedIn ? (
        <div>
          <h2>Login to TaskWave</h2>
          <form onSubmit={handleSubmit}>
            <input
              type="text"
              name="username"
              placeholder="Enter username"
              value={formData.username}
              onChange={handleChange}
              required
            />
            <input
              type="password"
              name="password"
              placeholder="Enter password"
              value={formData.password}
              onChange={handleChange}
              required
            />
            <button
              type="submit"
            >
              Log In
            </button>
          </form>
        </div>
      ) : (
        <div>
          <h1>
            Welcome back, <span>{formData.username}</span>! 🚀
          </h1>
        </div>
      )}
    </div>
  );
}

```

</details> -->

<br>

---

<div align="center">
<a href="#" >NEXT SESSION ></a>
</div>

---
