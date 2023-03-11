<template>
    <section class="hero" id="hero">
      <div class="hero-tags">
        <h1 class="hero-tagline">Best of Care, Easy to reach everywhere.</h1>
        <p class="hero-desc">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero dolorum
          obcaecati, molestiae quis aspernatur porro exercitationem possimus et
          nam nihil.
        </p>
      </div>
      <div class="hero-btn">
        <button class="register-btn" type="button">Get started now!</button>
      </div>

      <div class="container">
  <div class="box box3">
    <img src='../assets/prescription.jpg' alt=''>
  </div>
  <div class="box box2">
    <img src='../assets/doctor.jpg' alt=''>
  </div>
  <div class="box box1">
    <img src='../assets/hivemed-logo.png' alt=''>
  </div>
  <div class="box box4">
    <img src='../assets/prescription2.jpg' alt=''>
  </div>
  <div class="box box5">
    <img src='../assets/pharmacy.jpg' alt=''>
  </div>
  <div class="box box6">
    <img src='../assets/pharmacy3.jpg' alt=''>
  </div>
  <div class="box box7">
    <img src='../assets/patient.jpg' alt=''>
  </div>
</div>
    </section>
</template>

<style scoped>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.hero {
    background: linear-gradient(to right,var(--bg-color),var(--secondary-color));
    height: 100vh;
    width: 100vw;
    margin: 0; 
    padding: 0;
}

.hero-tagline {
    padding-left: 3rem;
    font-weight: var(--bolder-font);
    font-size: 3rem;
    color: var(--primary-color);
    text-decoration: none;
    position: absolute;
    top: 45%;
}

.hero-btn {
    padding-left: 3rem;
    position: absolute;
    vertical-align: auto;
    padding-top: 26.5%;
}

.hero-desc {
    padding-left: 3rem;
    padding-right: 42%;
    font-weight: var(--bold-font);
    font-size: 1.5rem;
    color: var(--font-color);
    text-decoration: none;
    text-align: justify;
    position: absolute;
    top: 53%;
}

.register-btn {
    background-color: var(--primary-color);
    padding: 15px 35px;
    border-radius: 5px;
    border: none;
    font-weight: var(--bold-font);
    cursor: pointer;
    transition: var(--transition);
    color: var(--font-color);
}

.desc {
    display: flex;
    flex-direction: column;
}

.register-btn:hover {
    color: var(--primary-color);
    background-color: var(--secondary-bg-color);
    border-bottom: 2px solid var(--font-color);
}

.container {
  position: absolute;
  /* to get a regualr hexagon with clip-path use the same scale, width is sqrt(3) / 2 of the height  */
  width: calc(var(--size) * 0.866);
  height: var(--size);
}

.box {
  overflow: hidden;
  position: absolute;
  top: 100%;
  left: 625%;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  background: rgba(255, 255, 255, .5);
  clip-path: polygon(50% 0,100% 25%,100% 75%,50% 100%,0 75%,0 25%);
}
img {
  transform-origin: center;
  object-fit: contain;
  transition: all .5s ease-out;
}
.box1 img {
  height: 100vh;
  width: 17rem;
}
.box2 img {
  height: 100vh;
  width: 28.5rem;
}
.box3 img {
  height: 18rem;
  width: 100vw;
}
.box4 img {
  height: 15.5rem;
  width: 100vw;
}
.box5 img {
  height: 100vh;
  width: 25rem;
}
.box6 img {
  height: 18rem;
  width: 100vw;
}
.box7 img {
  height: 100vh;
  width: 25rem;
}
img::after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  background: rgba(0, 0, 0, .45);
  transition: all .5s ease-out;
}
img:hover {
  transform: scale(1.2);
}
img::after {
  background: rgba(0, 0, 0, 0);
}
 
.box2.box {
  transform: translate(calc(-50% - (var(--gap) / 2)), calc(-75% - (var(--gap) ) / 2 * 1.732));
}

.box3.box {
  transform: translate(calc(50% + (var(--gap)  / 2)), calc(-75% - (var(--gap) ) / 2 * 1.732));
}

.box4.box {
  transform: translate(calc(-100% - var(--gap) ), 0);
}

.box5.box {
  transform: translate(calc(100% + var(--gap) ), 0);
}

.box6.box {
  transform: translate(calc(-50% - (var(--gap)  / 2)), calc(75% + (var(--gap) ) / 2 * 1.732));
}

.box7.box {
  transform: translate(calc(50% + (var(--gap)  / 2)), calc(75% + (var(--gap) ) / 2 * 1.732));
}
</style>
