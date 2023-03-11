<template>
  <section class="doctors-section">
    <h2>Our Registered Doctors</h2>
    <div class="doctors-container">
      <div class="arrow left-arrow" @click="scrollLeft">
        <i class="fa-solid fa-chevron-left"></i>
      </div>
      <div class="doctors" ref="doctorsContainer">
        <div class="doctor-box" v-for="(doctor, index) in doctors" :key="index" :style="{transform: `translateX(${doctor.translateX}px)`}">
          <div class="doctor-box-info">
            <img :src="doctor.image" :alt="doctor.name + ' Image'">
            <h3>{{doctor.name}}</h3>
            <p>{{doctor.description}}</p>
            <p>{{doctor.hospital}}</p>
            <p>{{doctor.address}}</p>
          </div>
        </div>
      </div>
      <div class="arrow right-arrow" @click="scrollRight">
        <i class="fa-solid fa-chevron-right"></i>
      </div>
      <div class="doctor-btn"><a href="viewMore-btn"><button class="viewMore-btn">View More</button></a></div>
    </div>
  </section>
</template>
<script>
import doctorImage1 from "@/assets/doctor1.jpg"
import doctorImage2 from "@/assets/doctor2.png"

export default {
  data() {
    return {
      doctors: [
        {
          image: doctorImage1,
          name: "Dr. John Smith",
          description: "Specializes in Cardiology",
          hospital: "St. Mary's Hospital",
          address: "123 Main St, Anytown USA",
          translateX: 0
        },
        {
          image: doctorImage2,
          name: "Dr. Jane Doe",
          description: "Specializes in Pediatrics",
          hospital: "Children's Hospital",
          address: "456 Elm St, Anytown USA",
          translateX: 0
        },
        {
          image: doctorImage1,
          name: "Dr. William Brown",
          description: "Specializes in Neurology",
          hospital: "General Hospital",
          address: "789 Oak St, Anytown USA",
          translateX: 0
        },
        {
          image: doctorImage2,
          name: "Dr. Susan Green",
          description: "Specializes in Dermatology",
          hospital: "University Hospital",
          address: "101 Pine St, Anytown USA",
          translateX: 0
        },
        {
          image: doctorImage1,
          name: "Dr. Michael Lee",
          description: "Specializes in Cardiology",
          hospital: "Mount Sinai Hospital",
          address: "321 Main St, Anytown USA",
          translateX: 0
        },
        {
          image: doctorImage2,
          name: "Dr. Emily Wong",
          description: "Specializes in Dermatology",
          hospital: "Skin Hospital",
          address: "654 Elm St, Anytown USA",
          translateX: 0
        },
        {
          image: doctorImage1,
          name: "Dr. James Johnson",
          description: "Specializes in Oncology",
          hospital: "Cancer Center",
          address: "987 Oak St, Anytown USA",
          translateX: 0
        },
        {
          image: doctorImage2,
          name: "Dr. Sarah Davis",
          description: "Specializes in Gynecology",
          hospital: "Women's Hospital",
          address: "111 Pine St, Anytown USA",
          translateX: 0
        },
        {
          image: doctorImage1,
          name: "Dr. Robert Garcia",
          description: "Specializes in Urology",
          hospital: "Urology Center",
          address: "222 Oak St, Anytown USA",
          translateX: 0
        },
        {
          image: doctorImage2,
          name: "Dr. Kyla Minerva",
          description: "Specializes in Oncology",
          hospital: "Cancer Center",
          address: "987 Oak St, Anytown USA",
          translateX: 0
        }
        ],
      computed: {
        doctorWidth() {
          const doctorBox = this.$refs.doctorsContainer.querySelector('.doctor-box');
          const doctorBoxStyle = getComputedStyle(doctorBox);
          const doctorBoxWidth = doctorBox.offsetWidth + parseInt(doctorBoxStyle.marginLeft) + parseInt(doctorBoxStyle.marginRight);
          return doctorBoxWidth;
        },
        containerWidth() {
          const doctorsContainerStyle = getComputedStyle(this.$refs.doctorsContainer);
          const containerWidth = parseInt(doctorsContainerStyle.width);
          return containerWidth;
        },
        maxTranslateX() {
          const numDoctors = this.doctors.length;
          const maxTranslateX = -(numDoctors * this.doctorWidth - this.containerWidth);
          return maxTranslateX;
        }
      },
      methods: {
        scrollLeft() {
          if (this.doctors[0].translateX < 0) {
          this.doctors.forEach(doctor => {
          doctor.translateX += this.doctorWidth;
          })
          }
        },
        scrollRight() {
          if (this.doctors[this.doctors.length - 1].translateX > this.maxTranslateX) {
          this.doctors.forEach(doctor => {
          doctor.translateX -= this.doctorWidth;
          });
          }
        },
        handleResize() {
          this.doctors.forEach(doctor => {
        doctor.translateX = 0;
          });
          }
        },
      mounted() {
      window.addEventListener('resize', this.handleResize);
      },
      beforeDestroy() {
      window.removeEventListener('resize', this.handleResize);
    }
}}}
</script>

<style scoped>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.doctors-section {
  height: 75vh;
  width: 100vw;
  background: linear-gradient(var(--secondary-bg-color),var(--bg-color));
}
.doctors-section h2 {
  padding: 3rem 0;
  font-size: 2rem;
}
.doctors-container {
  display: flex;
  align-items: center;
  height: auto;
  width: 120rem;
  margin: 0;
  padding: 15rem 15rem 0 15rem;
}
.arrow {
  z-index: 1;
  position: relative;
  background-color: rgba(255, 255, 255, 0.8);
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: background-color 0.2s ease-in-out;
}

.arrow:hover {
  background-color: rgba(255, 255, 255, 0.5);
}

.left-arrow {
  border-top-left-radius: 10px;
  border-bottom-left-radius: 10px;
}

.right-arrow {
  border-top-right-radius: 10px;
  border-bottom-right-radius: 10px;
}

.doctors {
  width: auto;
  display: inline-block;
  white-space: nowrap;
  overflow-x: scroll;
  overflow-y: hidden;
  -webkit-overflow-scrolling: touch;
  margin: .5rem;
  border: solid var(--primary-color);
  border-radius: 10px;
  height: 30rem;
  margin-top: -15rem;
}

.doctor-box {
  width: 15rem;
  height: 25rem;
  display: inline-block;
  vertical-align: top;
  background-color: var(--secondary-bg-color);
  border-radius: 15px;
  padding: 3rem 0;
  margin: 2rem 5rem;
}

.doctor-box img {
  width: 100%;
  border-radius: 50%;
}

.doctor-box-info h3 {
  margin-top: 1rem;
}

.doctor-box-info p {
  padding: .25rem;
}

.viewMore-btn {
    border-radius: 50%;
    padding: 15px 40px;
    background-color: var(--primary-color);
    border: none;
    border-radius: 50px;
    cursor: pointer;
    transition: var(--transition);
    font-weight: var(--bold-font);
    color: var(--font-color);
}
.doctors-section button {
position: absolute;
bottom: -100rem;
left: 50%;
transform: translateX(-50%);
}


@media only screen and (max-width: 768px) {
  .doctors-container {
    flex-wrap: wrap;
  }

  .doctor-box {
    width: 100%;
    margin-right: 0;
    margin-bottom: 20px;
  }
}
</style>