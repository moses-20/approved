# APPROVAL1 Project

## Introduction
By following instructions below, you will build the inventory, contact and footer sections of the webpage.

## Getting Started
You must have completed Lesson 1 before continuing.

### Objectives
- building inventory section
- creating contact section
- adding footer to the webpage


### ⚠️ It is advised that you type the code yourself. By so doing, you will understand better.
---

#### **Building inventory section**
1. **index.html**: type the code below after the ending `</div>` tag before `</main>`
```
<!-- inventory section -->
<section id="inventory" class="py-2">
  <div class="container inventory-inner">
    <div class="centered py-3">
      <h1 class="title-dark">Our inventory</h1>
    </div>

    <p class="lead centered">
      We offer huge variety of vehicles which you can enjoy
    </p>

    <div class="col-4 py-3">
      <div class="box">
        <div class="vehicle">
          <img src="img/svg/car.svg" alt="" />
        </div>
        <div class="description">
          <h1>Cars</h1>
          <p class="lead">
            From fuel efficient commuters to high powered sports cars and
            luxury sedans, we can help you find the perfect car for your
            situation.
          </p>
          <a href="#" class="btn-apply-dark">Apply now</a>
        </div>
      </div>

      <div class="box">
        <div class="vehicle">
          <img src="img/svg/minivan.svg" alt="" />
        </div>
        <div class="description">
          <h1>Minivans</h1>
          <p class="lead">
            With seating for up to 7 and plenty of room for whatever you
            may need to transport, a minivan makes the perfect family
            vehicle.
          </p>
          <a href="#" class="btn-apply-dark">Apply now</a>
        </div>
      </div>

      <div class="box">
        <div class="vehicle">
          <img src="img/svg/truck.svg" alt="" />
        </div>
        <div class="description">
          <h1>Trucks</h1>
          <p class="lead">
            Need to haul a trailer, just like helping your friends move?
            Our dealers carry a wide variety of midsize and full-size
            trucks from various manufacturers.
          </p>
          <a href="#" class="btn-apply-dark">Apply now</a>
        </div>
      </div>

      <div class="box">
        <div class="vehicle">
          <img src="img/svg/suv.svg" alt="" />
        </div>
        <div class="description">
          <h1>SUVs</h1>
          <p class="lead">
            Looking for something suitable for city driving, but still
            want that off-road capability? Let us help you get into the
            perfect SUV. Compact to full-size, we have it!
          </p>
          <a href="#" class="btn-apply-dark">Apply now</a>
        </div>
      </div>
    </div>
  </div>
</section>
```

2. **css/main.css**: add the following code
```
/* style rules for inventory section */

#inventory {
  background: #f3eff5;
  color: #1f333b;
  height: auto;
  padding-bottom: 8rem;
}

#inventory .inventory-inner .col-4 {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 2rem;
}

#inventory .inventory-inner .col-4 .box {
  color: #1f333b;
  background: #effaff;
  box-shadow: 0 2px 7px 2px rgba(0, 0, 0, 0.1);
  transition: transform 0.5s;
  border-radius: 10px;
  text-align: center;
  max-width: 25vw;
}

#inventory .inventory-inner .col-4 .box:hover {
  transform: scale(1.03);
}

#inventory .inventory-inner .col-4 .box .vehicle {
  background: #24527e;
  border-radius: 10px 10px 0 0;
  padding: 1rem;
}

#inventory .inventory-inner .col-4 .box .vehicle img {
  max-width: 100px;
  height: auto;
}

#inventory .inventory-inner .col-4 .box .description {
  display: grid;
  grid-template-rows: fit-content(4rem) 11rem 1fr;
  row-gap: 1rem;
  justify-items: center;
  padding: 1rem;
}
```

3. **terminal**: run the following one after the other
```
git status
git add .
git commit -m "lesson-2: added inventory section"
```
4. Your webpage should look like the image below

![inventory](img/inventory.png)
---

#### **Creating contact section**
1. **index.html**: add the following after the closing `</section>` tag before `</main>`
```
<!-- contact section -->
<section id="contact">
  <div class="container contact-inner">
    <div class="centered py-2">
      <h1 class="title-light">Contact us</h1>
    </div>

    <p class="lead centered">
      Got any questions? Just want to say hello? Feel free to contact us!
    </p>

    <div class="col-2">
      <div class="col-left">
        <form method="POST" class="py-2">
          <div class="contact-email">
            <label for="email">Email</label>
            <input
              required
              type="email"
              name="email"
              id="email"
              class="email-input"
              placeholder="Enter your email"
            />
          </div>

          <div class="contact-name">
            <label for="name">Name</label>
            <input
              required
              type="text"
              name="name"
              id="name"
              class="name-input"
              placeholder="Enter your name"
            />
          </div>

          <div class="contact-text">
            <label for="message">Message</label>
            <textarea
              required
              name="message"
              id="message"
              class="message-input"
              placeholder="Enter a message"
            ></textarea>
          </div>

          <button type="submit" class="btn-apply-light">
            Send a message
          </button>
        </form>
      </div>

      <div class="col-right py-2">
        <h2>Our informations</h2>
        <p>You can also reach out using:</p>

        <ul class="contact-data py-1">
          <li>
            <p>
              <i data-feather="phone"></i>
              <span>
                <strong>323-776-2888</strong>
              </span>
            </p>
          </li>

          <li>
            <p>
              <i data-feather="mail"></i>
              <span>
                <strong>hello@approval1.com</strong>
              </span>
            </p>
          </li>

          <li>
            <p>
              <i data-feather="map-pin"></i>
              <span>
                <strong
                  >4341 Kennedy Court, Westlake Village, CA, 91361</strong
                >
              </span>
            </p>
          </li>
        </ul>
      </div>
    </div>
  </div>
</section>
```

2. **css/main.css**
```
/* style rules for contact section */
#contact {
  background: #24527e;
  color: #effaff;
  height: 70vh;
  z-index: 1;
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

#hero::before,
#contact::before {
  z-index: -1;
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  background: inherit;
  transform: skewY(-3deg);
}

#contact::before {
  box-shadow: 0 -8px 6px -2px rgba(0, 0, 0, 0.25);
  transform-origin: top left;
}

#contact .contact-inner .col-2 .col-left form .contact-email .email-input,
#contact .contact-inner .col-2 .col-left form .contact-name .name-input,
#contact .contact-inner .col-2 .col-left form .contact-text .message-input {
  border-radius: 3px;
  box-shadow: 0 2px 7px 2px rgba(0, 0, 0, 0.1);
  padding: 1rem 1rem;
  font-size: inherit;
  font-family: inherit;
  width: 100%;
  transition: 0.5s;
  outline: none;
}

#contact .contact-inner .col-2 {
  display: grid;
  grid-template-columns: 2fr 1fr;
  grid-gap: 1rem;
}

#contact .contact-inner .col-2 .col-left form {
  display: grid;
  grid-template-areas:
    "email name"
    "message message";
  grid-gap: inherit;
}

#contact .contact-inner .col-2 .col-left form .contact-email {
  grid-area: email;
}
```

3. **terminal**: run the following one after the other
```
git status
git add .
git commit -m "lesson-2: created contact section"
```
4. Compare your output with the image below

![contact](/img/contact.png)
---

#### **Adding footer to the page**
1. **index.html**: add the code after the closing `</main>` tag
```
<!-- footer -->
<footer>
  <div class="container footer-inner">
    <div class="credits">
      <h3>&copy; 2021</h3>
    </div>
    <div class="logo">
      <a href="#hero" aria-label="Get back to the top of the page">
        <img src="img/logo.png" alt="APPROVAL1" />
      </a>
    </div>
  </div>
</footer>
```

2. **css/main.css**:
```
footer {
  height: auto;
  background: #effaff;
}
footer .footer-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

3. **terminal**: run the following one after the other
```
git status
git add .
git commit -m "lesson-2: added footer to page"
```

## Observations
Write out the observations you made.


## Next Steps
Scroll to the top and click **master**. Select **lesson-3** to continue. <br /> ![continuation](img/master.png)