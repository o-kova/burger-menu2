# burger-menu2

/_ header start _/
.header {
flex-basis: 3.18%;
background-color: #ffffff;
position: sticky;
top: 0;
width: 100%;
}

.header\_\_container {
display: flex;
justify-content: space-between;
align-content: center;
align-items: center;
padding: 3.5rem 1rem 3.5rem 0;

@media screen and (max-width: 769px) {
padding: 2rem 1rem 2rem 0;
}
}

.header\_\_logo {
align-self: center;

@media screen and (max-width: 769px) {
order: 1;
}
}

.header\_\_img {
width: 4rem;

@media screen and (max-width: 769px) {
width: 5rem;
}
}

.header\_\_nav {
width: 100%;
height: 100%;
position: fixed;
background-color: #fff;
overflow: hidden;

@media screen and (max-width: 769px) {
margin-top: 26rem; //4rem
}
@media screen and (max-width: 361px) {
margin-top: 40rem; //4rem
}
}

.header\_\_list {
display: flex;
justify-content: space-between;
align-content: center;
width: 40%;

@media screen and (max-width: 769px) {
display: flex;
flex-direction: column;
justify-content: center;
padding-left: 40%;
}

@media screen and (max-width: 361px) {
padding-left: 30%;
}
}

.header a {
text-decoration: none;
}

.header\_\_item {
list-style: none;
}

.header\_\_link {
display: block;
padding: 30px;
color: $header;
text-align: center;
width: 8rem;
}

.header\_\_link:hover {
color: $btn;
}

.header**nav {
max-height: 0;
transition: max-height 0.5s ease-out;
}
.header**hamb {
cursor: pointer;
float: left;
padding: 23px;
} /_ Style label tag _/

.header\_\_hamb-line {
background: $text;
border-radius: 0.1875rem;
display: block;
height: 2px;
position: relative;
width: 24px;
} /_ Style span tag _/

.header**hamb-line::before,
.header**hamb-line::after {
background: $text;
border-radius: 0.1875rem;
content: "";
display: block;
height: 110%;
position: absolute;
transition: all 0.2s ease-out;
width: 100%;
}
.header**hamb-line::before {
top: 5px;
}
.header**hamb-line::after {
top: -5px;
}

.header\_\_side-menu {
display: none;
} /_ Hide checkbox _/

/_ Toggle menu icon _/
.header**side-menu:checked ~ .header**nav {
max-height: 100%;
}
.header**side-menu:checked ~ .header**hamb .header**hamb-line {
background: transparent;
}
.header**side-menu:checked ~ .header**hamb .header**hamb-line::before {
transform: rotate(-45deg);
top: 0;
}
.header**side-menu:checked ~ .header**hamb .header\_\_hamb-line::after {
transform: rotate(45deg);
top: 0;
}

@media screen and (min-width: 769px) {
.header\_\_nav {
max-height: none;
top: 0;
position: relative;
float: right;
width: fit-content;
}

.header\_\_item {
float: left;
}

.header\_\_link:hover {
background-color: transparent;
color: $btn;
}

.header\_\_hamb {
display: none;
}
}

/_ button _/
.header\_\_btn-container {
@media screen and (max-width: 769px) {
order: 2;
}
}

.header\_\_btn {
display: inline-block;
/_ margin: 0 14px 0 12px; _/
}
/_ header end _/

<header class="header">
      <div class="header__container container">
        <!-- logo -->
        <a href="#" class="header__logo"
          ><img
            src="./assets/images/logo-mob.jpg"
            class="header__img"
            alt="ФБД"
        /></a>
        <!-- hamburger icon -->
        <input class="header__side-menu" type="checkbox" id="side-menu" />
        <label class="header__hamb" for="side-menu"
          ><span class="header__hamb-line"></span
        ></label>
        <!-- menu -->
        <nav class="header__nav">
          <ul class="header__list">
            <li class="header__item">
              <a href="#" class="header__link">ДиабетФест</a>
            </li>
            <li class="header__item">
              <a href="#" class="header__link">Наши Достижения</a>
            </li>
            <li class="header__item">
              <a href="#" class="header__link">Партнеры</a>
            </li>
          </ul>
        </nav>
        <div class="header__btn-container">
          <div class="header__btn">
            <a href="#" class="header__btn-link button">Помочь</a>
          </div>
        </div>
      </div>
    </header>