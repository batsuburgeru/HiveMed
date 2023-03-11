<template>
    <nav>
         <a href="#hero" class="logo"><h1 class="logo">HiveMed</h1></a>
      <ul class="navbar">
        <li><a href="#" class="navbar-links">Book an Appointment</a></li>
        <li>
          <a href="#" class="navbar-links">Doctors</a>
        </li>
        <li><a href=" " class="navbar-links">Pharmacies</a></li>
        <li>
          <a href="#" class="navbar-links">About Us</a>
        </li>
      </ul>
      <a href="nav-button"><button class="nav-button">Login</button></a>
    </nav>
</template>

<style scoped>
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
ul {
    list-style-type: none;
}

a {
    text-decoration: none;
    color:var(--primary-color)
}

nav {
    width: 100vw;
    top: 0;
    left: 0;
    padding: 1rem 3.5rem;
    z-index: 1;
    position: sticky;
    box-sizing: border-box;
    display: flex;
    align-items: center;
    justify-content: space-between;
    box-shadow: 0 3px 5px rgba(0, 0, 0, 0.3);
    background-color: var(--secondary-bg-color);
}

.logo {
    margin-right: auto;
}
nav a {
    color: var(--primary-color);
    transition: var(--transition);
}

nav ul {
    display: flex;
    gap: 2rem;
}

nav ul li {
    font-weight: var(--bold-font);
    margin-right: 1rem;
}

nav a:hover{
    color: var(--secondary-color);
    border-bottom: 2px solid var(--font-color);
}

.nav-button {
    border-radius: 50%;
    padding: 9px 25px;
    background-color: var(--primary-color);
    border: none;
    border-radius: 50px;
    cursor: pointer;
    transition: var(--transition);
    font-weight: var(--bold-font);
    color: var(--font-color);
}
</style>