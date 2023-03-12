<template>
    <section id="descSection" class="desc">
  <div class="brief-desc">
    <h2>Why Choose HiveMed?</h2>
    <p>
      HiveMed represents a revolutionary leap forward in the medical industry, bringing together the key players of pharmacies, doctors, and users in a seamless, intuitive platform. Utilizing state-of-the-art AI technology, we provide unparalleled accuracy and reliability in the information we offer regarding prescribed drugs, ensuring the utmost confidence and peace of mind for all parties involved. With our user-friendly interface, locating the nearest pharmacy and checking drug availability is a breeze, empowering our users with the ability to make informed decisions regarding their healthcare. Our registered doctors enjoy the convenience of electronically passing prescriptions to registered pharmacies, streamlining the process and ensuring optimal efficiency. And with our intuitive chat functionality, communication between doctors and patients has never been easier or more accessible. At HiveMed, we are committed to leveraging technology to enhance the healthcare experience for all, and we are proud to be leading the charge towards a brighter, more connected future.
    </p>
  </div>
  <div class="graphic-desc">
    <div class="icon-wrapper">
      <img class="desc-icon" src="../assets/icons8-bot.gif" alt="AI" />
      <img class="desc-icon" src="../assets/icons8-computer-chat.gif" alt="Computer Chat" />
      <img class="desc-icon" src="../assets/icons8-hand-with-a-pill.gif" alt="Hand with a Pill" />
      <img class="desc-icon" src="../assets/icons8-online-payment.gif" alt="Online Payment" />
      <img class="desc-icon" src="../assets/icons8-stethoscope.gif" alt="Stethoscope Icon" />
    </div>
  </div>
  <div class="benefits"></div>
</section>
</template>

<style scoped>
*{
  margin: 0;
  padding: 0;
}

.desc {
  background-color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 3rem;  
}

.brief-desc {
  text-align: justify;
  margin-bottom: 3rem;
}

.brief-desc h2 {
  margin-top: 2rem;
  color: #3e3e3e;
  font-size: 2.5rem;
  margin-bottom: 1rem;
  padding-top: 2rem;
}

.brief-desc p {
  color: #3e3e3e;
  font-size: 1.2rem;
  line-height: 1.5;
  max-width: 60rem;
  margin: 0 auto;
}

.graphic-desc {
  text-align: center;
  margin-bottom: 3rem;
}

.icon-wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  max-width: 80rem;
  margin: 0 auto;
}

.desc-icon {
  width: 8rem;
  height: 8rem;
  border-radius: 50%;
  background-color: white;
  border: 2px solid #3e3e3e;
  padding: 1.5rem;
  margin: 1rem;
  box-shadow: 0px 2px 8px rgba(0, 0, 0, 0.15);
  transition: transform 0.3s ease-in-out;
}

.desc-icon:hover {
  transform: translateY(-10px);
}

.desc-icon img {
  width: 100%;
  height: 100%;
}

@media screen and (max-width: 768px) {
  .brief-desc p {
    font-size: 1rem;
    max-width: 100%;
    padding: 0 1.5rem;
  }

  .desc-icon {
    width: 6rem;
    height: 6rem;
  }
}
</style>