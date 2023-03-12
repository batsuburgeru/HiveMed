<template>
  <!-- Footer -->
  <MDBFooter :text="['center', 'lg-start', 'muted']">
    <!-- Section: Social media -->
    <section class="
        d-flex
        justify-content-center justify-content-lg-between
        p-4
        border-bottom
      ">
      <!-- Left -->
      <div class="me-5 d-none d-lg-block">
        <span>Get connected with us on social networks:</span>
      </div>
      <!-- Left -->
      <!-- Right -->
      <div>
        <a href="" class="me-4 text-reset">
          <MDBIcon iconStyle="fab" icon="facebook-f"></MDBIcon>
        </a>
        <a href="" class="me-4 text-reset">
          <MDBIcon iconStyle="fab" icon="twitter"></MDBIcon>
        </a>
        <a href="" class="me-4 text-reset">
          <MDBIcon iconStyle="fab" icon="google"></MDBIcon>
        </a>
        <a href="" class="me-4 text-reset">
          <MDBIcon iconStyle="fab" icon="instagram"></MDBIcon>
        </a>
        <a href="" class="me-4 text-reset">
          <MDBIcon iconStyle="fab" icon="linkedin"></MDBIcon>
        </a>
        <a href="" class="me-4 text-reset">
          <MDBIcon iconStyle="fab" icon="github"></MDBIcon>
        </a>
      </div>
      <!-- Right -->
    </section>
    <!-- Section: Social media -->
    <!-- Section: Links  -->
    <section class="">
      <MDBContainer class="text-center text-md-start mt-5">
        <!-- Grid row -->
        <MDBRow class="mt-3">
          <!-- Grid column -->
          <MDBCol md="3" lg="4" xl="3" class="mx-auto mb-4">
            <!-- Content -->
            <h6 class="text-uppercase fw-bold mb-4">
              <i class="fas fa-gem me-3"></i>HiveMed
            </h6>
            <p>
              Copyright © 2023 HiveMed. All rights reserved. This website is designed and developed by HiveMed and is powered by VueJs, HTML, CSS. Privacy Policy | Terms of Use
            </p>
          </MDBCol>
          <!-- Grid column -->
          <!-- Grid column -->
          <MDBCol md="2" lg="2" xl="2" class="mx-auto mb-4">
            <!-- Links -->
            <h6 class="text-uppercase fw-bold mb-4">Register Here</h6>
            <p>
              <a href="#!" class="text-reset">Doctors</a>
            </p>
            <p>
              <a href="#!" class="text-reset">Pharmacies</a>
            </p>
            <p>
              <a href="#!" class="text-reset">Register Here</a>
            </p>
          </MDBCol>
          <!-- Grid column -->
          <!-- Grid column -->
          <MDBCol md="3" lg="2" xl="2" class="mx-auto mb-4">
            <!-- Links -->
            <h6 class="text-uppercase fw-bold mb-4">Useful Links</h6>
            <p>
              <a href="#!" class="text-reset">Pricing</a>
            </p>
            <p>
              <a href="#!" class="text-reset">Settings</a>
            </p>
            <p>
              <a href="#!" class="text-reset">About Us</a>
            </p>
            <p>
              <a href="#!" class="text-reset">FAQ</a>
            </p>
          </MDBCol>
          <!-- Grid column -->
          <!-- Grid column -->
          <MDBCol md="4" lg="3" xl="3" class="mx-auto mb-md-0 mb-4">
            <!-- Links -->
            <h6 class="text-uppercase fw-bold mb-4">Contact</h6>
            <p>
              <i class="fas fa-home me-3"></i> 363 Pascual Casal St, Quiapo, Manila, 1001 Metro Manila
            </p>
            <p>
              <i class="fas fa-envelope me-3"></i>
              HiveMed@email.com
            </p>
            <p>
              <MDBIcon icon="phone" class="me-3" /> +63 1234567890
            </p>
            <p>
              <MDBIcon icon="print" class="me-3" /> 555 123 4567
            </p>
          </MDBCol>
          <!-- Grid column -->
        </MDBRow>
        <!-- Grid row -->
      </MDBContainer>
    </section>
    <!-- Section: Links  -->
    <!-- Copyright -->
    <div class="text-center p-4" style="background-color: rgba(0, 0, 0, 0.05)">
      © 2023 Copyright:
      <a class="text-reset fw-bold" href="https://mdbootstrap.com/">HiveMed.com</a>
    </div>
    <!-- Copyright -->
  </MDBFooter>
  <!-- Footer -->
</template>

<script>
  import {
    MDBFooter,
    MDBContainer,
    MDBRow,
    MDBCol,
    MDBIcon
  } from 'mdb-vue-ui-kit';

  export default {
    components: {
      MDBFooter,
      MDBContainer,
      MDBRow,
      MDBCol,
      MDBIcon
    },
  };
</script>

<style scoped>
@import 'mdb-vue-ui-kit/css/mdb.min.css';
</style>