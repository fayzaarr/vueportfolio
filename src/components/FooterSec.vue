<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="brand">
        <h2 class="blankafont">
          RFSYNYZ
          <p>Rifasya Ayu Nurfayza</p>
        </h2>
        <div class="desc-footer">
          Available to discuss opportunities—reach <br>out as needed.
        </div>
      </div>
      <div class="nav-social">
        <nav class="nav-links">
          <a href="#section-home" @click.prevent="scrollToSection('section-home')">Home</a>
          <a href="#section-profile" @click.prevent="scrollToSection('section-profile')">About</a>
          <a href="#section-projects" @click.prevent="scrollToSection('section-projects')">Projects</a>
          <a href="#section-services" @click.prevent="scrollToSection('section-services')">Services</a>
          <a href="#section-contact" @click.prevent="scrollToSection('section-contact')">Contact</a>
        </nav>
        <div class="social-icons">
          <a href="https://github.com/fayzaarr" target="_blank"><img src="@/assets/icon/logo(white).png" alt="GitHub"></a>
          <a href="https://www.linkedin.com/in/rifasyaanr/" target="_blank"><img src="@/assets/icon/linkedin(white).png" alt="LinkedIn"></a>
          <a href="https://www.instagram.com/rfssyar_" target="_blank"><img src="@/assets/icon/social.png" alt="Instagram"></a>
          <a href="https://mail.google.com/mail/?view=cm&fs=1&to=nurfayza.rr@gmail.com&su=Hello&body=I would like to reach out..."><img src="@/assets/icon/email(white).png" alt="Email"></a>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <hr>
      <p>&copy; 2025 RFSYNYZ. All rights reserved</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterSection",
  methods: {
    scrollToSection(id) {
      const section = document.getElementById(id);
      if (section) {
        section.scrollIntoView({ behavior: "smooth" });
      }
    },
  }
};
</script>

<style scoped>
@font-face {
  font-family: 'Blanka';
  src: url('@/assets/fonts/blanka/BLANKA Font/Blanka-Regular.otf') format('opentype');
  font-weight: normal;
  font-style: normal;
}

.footer {
  background: #0d0e0e;
  color: #fff;
  padding-top: 3vw;
  text-align: center;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  padding-bottom: 10px;
  padding-left: 5vw;
  padding-right: 5vw;
}

.desc-footer {
  margin-top: 4vh;
  font-size: 1vw;
  text-align: left;
}

.brand h2 {
  margin: 0;
  text-align: left;
  font-size: 40px;
}

.brand p {
  margin: 0;
  text-align: left;
  font-size: 16px;
  font-family: Arial, Helvetica, sans-serif;
}

.blankafont {
  font-family: 'Blanka', sans-serif;
}

.nav-social {
  display: flex;
  flex-direction: column;
  margin-top: -50px;
}

.nav-links a {
  color: white;
  margin: 0 25px;
  text-decoration: none;
  font-weight: bold;
  font-size: 1vw;
}

.nav-links a:hover {
  text-decoration: underline;
}

.social-icons {
  display: flex; 
  justify-content: flex-end; 
  align-items: center;
  margin: 20px 0;
}

.social-icons img {
  width: 50%;
  height: 50%;
}

.social-icons a:hover {
  transform: scale(1.2); 
}

.footer-bottom hr {
  line-height: 1px;
  width: 90%;
  color: #eeedf4;
}

.footer-bottom {
  border-top: 1px solid #0d0e0e;
  padding-top: 4vw;
  font-size: 0.8vw;
  padding-bottom: 1px;
}

@media screen and (max-width: 768px) {
  .footer-content {
    flex-direction: column;
    align-items: center;
    padding: 20px;
    gap: 10vw;
    text-align: center;
  }

  .brand h2,
  .brand p,
  .desc-footer {
    text-align: center;
  }

  .brand h2 {
    font-size: 25px;
  }

  .brand p {
    font-size: 10px;
  }

  .desc-footer {
    font-size: 0.8rem;
    margin-top: 2vh;
    margin-bottom: 2vh;
  }

  .nav-links {
    display: flex;
    gap: 10px;
  }

  .nav-links a {
    font-size: 0.8rem;
    margin: 0;
  }

  .social-icons {
    justify-content: center;
    gap: 15px;
    flex-wrap: wrap;
  }

  .social-icons img {
    width: 30px;
    height: 30px;
  }

  .footer-bottom {
    font-size: 0.7rem;
    padding-top: 0;
  }
}

</style>
