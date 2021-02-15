# APPROVAL1 Project

## Introduction
By following instructions on this branch, you will build the navigation and banner section of the page.

![approval home](/img/home.png "approval home")

## Getting Started
Ensure you have the following done
1. VS Code (with Live Server) installed
2. Git and Github configured
3. Set up a project folder ( named **approval**)

I have created a starter template for you, copy and paste the code below in the terminal of your VS Code to get it.
```
git clone -b approved --single-branch https://github.com/armaebii/approved.git .
```


### Objectives
- building the navigation
- adding banner section
- creating about section


### ⚠️ It is advised that you type the code yourself. By so doing, you will understand better.
---

#### **Building the navigation**
1. **index.html**: Between the `body` tags, replace the `h1` element with the following code:
```
<!-- navigation -->
  <nav id="navbar">
    <div class="container navbar-inner">
      <!-- logo -->
      <div class="logo">
        <a href="#hero">
          <img src="img/logo.png" alt="APPROVAL1" />
        </a>
      </div>

      <!-- navigation links -->
      <ul class="links">
        <li><a href="#about">About us</a></li>
        <li><a href="#inventory">Inventory</a></li>
        <li><a href="#contact">Contact us</a></li>
        <li>
          <a href="#" class="btn-apply-dark">Apply now</a>
        </li>
      </ul>

      <!-- menu icon -->
      <div class="hamburger" onclick="showMenu()">
        <i data-feather="menu"></i>
      </div>
    </div>
  </nav>
```

2. **css/main.css**: add the following code
```
/* style rules for navigation */
.logo {
  display: flex;
  align-items: center;
  width: 175px;
  height: auto;
}

#navbar {
  height: auto;
  position: sticky;
  top: 0;
  z-index: 10;
  background: #effaff;
  box-shadow: none;
  transition: box-shadow 0.5s;
}

#navbar .navbar-inner {
  display: flex;
  justify-content: space-between;
}

#navbar .navbar-inner .hamburger {
  display: none;
}

#navbar .navbar-inner .links {
  display: flex;
}

#navbar .navbar-inner .links li {
  padding: 1.5rem 1.5rem;
}

#navbar .navbar-inner .links li:last-child {
  padding: 0.75rem 1.5rem;
}

#navbar .navbar-inner .links li a {
  font-weight: 800;
  text-decoration: none;
  color: #1f333b;
  text-transform: uppercase;
}
```

3. **terminal**: run the following one after the other
```
git status
git add .
git commit -m "lesson-1: built navigation bar"
```
---

#### **Adding banner section**
1. **index.html**: add the following after the `</nav>` closing tag
```
<!-- banner -->
<header id="hero">
  <div class="container hero-inner">
    <!-- leading text -->
    <div class="heading animated fadeIn">
      <h1>Start driving your credit.</h1>
      <p class="lead py-1">
        No Appointments, no obligation and free to apply. Are you looking
        for a new car?
      </p>
      <a href="#" class="btn-apply-light">Get a car now</a>
    </div>

    <!-- banner image -->
    <div class="car animated fadeIn">
      <img src="img/svg/hero-car.svg" alt="car" />
    </div>
  </div>
</header>
```

2. **css/main.css**
```
/* style rules for banner section */
#hero {
  position: relative;
  background: #24527e;
  color: #effaff;
  height: 80vh;
  z-index: 1;
}

#hero::before {
  transform-origin: right bottom;
  box-shadow: 0 8px 6px -2px rgba(0, 0, 0, 0.25);
}

#hero .hero-inner {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  height: inherit;
  align-items: center;
}
```

3. **terminal**: run the following one after the other
```
git status
git add .
git commit -m "lesson-1: added banner section"
```
---

#### **Creating about section**
1. **index.html**: add the following after the closing `</header>` tag
```
<!-- main content -->
<main>
  <!-- about section -->
  <section id="about" class="py-2">
    <div class="container about-inner">
      <div class="centered py-3">
        <h1 class="title-dark">About us</h1>
      </div>

      <div class="about-grid">
        <p class="about-left lead">
          Founded in 2019 by Micheal, Approval1 has come a long way from its
          beginnings in California. When our team first started out, their
          passion for cars drove them to quit day job so that Approval1 can
          offer you the world's most best service. We now serve customers
          all over country, and are thrilled that we're able to turn our
          passion into our own website.
        </p>
        <img src="img/svg/about.svg" alt="About us" class="py-1" />
      </div>
    </div>
  </section>

  <!-- division line -->
  <div id="hr">
    <hr class="container" />
  </div>
</main>
```

2. **css/main.css**
```
/* style rules for about section */
#about {
  z-index: -1;
  background: #f3eff5;
  color: #1f333b;
  height: auto;
}
#about .about-inner .about-grid {
  display: grid;
  align-items: center;
  grid-template-columns: 2fr 1fr;
}
#about .about-inner .about-grid .about-left {
  padding-right: 2rem;
}
```

3. **terminal**: run the following one after the other
```
git status
git add .
git commit -m "lesson-1: created about section"
```
---

## Observations
Write out the observations you made.


## Next Steps
Scroll to the top and click **master**. Select **lesson-2** to continue. <br /> ![continuation](img/master.png)