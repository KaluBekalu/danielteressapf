<template>
  <div id="about" class="about">
    <div class="banner">
      <img src="../assets/bimg.png" alt="" />
      <div class="cliped">
        <h1>About</h1>
      </div>
      <div class="info">
        <div class="info-top">
          <h1>{{ personalInfo.fullName }}</h1>
          <span></span>
          <p>{{ personalInfo.currentPosition }}</p>
        </div>
        <div class="info-address">
          <i class="fa-solid fa-briefcase"></i>
          <p>{{ personalInfo.office }}</p>
        </div>
        <div class="info-address">
          <i class="fa-regular fa-envelope"></i>
          <p>{{ personalInfo.email }}</p>
        </div>
        <div class="info-address">
          <i class="fa-regular fa-envelope"></i>
          <p>{{ personalInfo.email2 }}</p>
        </div>
      </div>
      <div class="message">
        <p>
          Hello, <br />
          <br />
          {{ personalInfo.message }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: { personalInfo: { type: Object } },
};
</script>

<style>
.about {
  margin-top: 5rem;
  margin-bottom: 4rem;
}
#about::before {
  display: block;
  content: "";
  height: 5rem;
  background: #13293e;
}

.cliped > h1 {
  text-align: center;
  color: #fff;
  /* margin-top: 10px; */
}
.banner {
  width: 100%;
  height: 32rem;
  position: relative;
  overflow: hidden;
}
.cliped {
  width: 100%;
  height: 100%;
  background: #13293e;
  clip-path: polygon(0% 0%, 100% 0, 100% 65%, 50% 65%);
}
.banner img {
  position: absolute;
  z-index: 10;
  width: 25rem;
  bottom: -80px;
  left: 4%;
}
.banner .message {
  position: absolute;
  width: 60%;
  max-width: 50rem;
  bottom: 0;
  right: 0%;
}
.info {
  position: absolute;
  right: 9.8rem;
  top: 20%;
  color: #fff;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  align-items: self-start;
}

.info-top {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 0.5rem;
}

.info-top p {
  font-size: 1.5rem;
  font-weight: 100;
}
.info-top span {
  height: 2rem;
  width: 1px;
  background: #fff;
}
.info-top h1 {
  margin: 0;
}

.info-address {
  display: flex;
  gap: 1rem;
  align-items: baseline;
  font-weight: 200;
  font-size: 1.2rem;
  letter-spacing: 2px;
}

@media (max-width: 1300px) {
  .info {
    right: 9rem;
  }
  .banner img {
    width: 22rem;
    bottom: -10px;
  }
}
@media (max-width: 1200px) {
  .info-top h1 {
    font-weight: 400;
  }
  .info-top h1,
  .info-top p {
    font-size: 1.2rem;
  }
  .info-top span {
    height: 1.4rem;
  }
  .info-address {
    font-size: 1rem;
  }
  /* .banner .message {
    right: 15%;
  } */
  .banner img {
    width: 20rem;
  }
}
@media (max-width: 1050px) {
  /* .banner .message {
    right: 10%;
  } */
  .info {
    right: 9rem;
  }
}
@media (max-width: 1000px) {
  .banner img {
    width: 20rem;

    left: 0;
  }
  .message {
    width: 22rem;
    font-size: 0.9rem;
  }
}
@media (max-width: 900px) {
  .info {
    right: 5rem;
  }

  .banner {
    height: 25rem;
    width: 100%;
  }
  .banner img {
    width: 18rem;
    bottom: 0px;
    left: 0;
  }
  .cliped {
    height: 90%;
  }

  .info {
    right: 40px;
  }
}

@media (max-width: 750px) {
  .banner img {
    width: 17rem;
  }
}
@media (max-width: 700px) {
  .banner img {
    bottom: unset;
    width: 11.1rem;
    clip-path: polygon(0% 0%, 100% 0%, 100% 90%, 0% 90%);
  }
  .info-top h1,
  .info-top p {
    font-size: 1rem;
  }
  .info-address {
    font-size: 0.8rem;
  }
  .banner .message {
    width: 90%;
    left: 20px;
    bottom: 0;
    top: unset;
    font-size: 0.8rem;
  }
  @media (max-width: 600px) {
    .info {
      right: 10px;
    }
    .info-top h1,
    .info-top p {
      font-size: 0.8rem;
    }
    .cliped {
      clip-path: polygon(0% 0%, 100% 0, 100% 65%, 40% 65%);
    }
  }
}
@media (max-width: 470px) {
  .info {
    top: 10%;
    right: 0;
  }
  .info-top h1,
  .info-top p,
  .info-address {
    font-size: 0.6rem;
  }
}
@media (max-width: 435px) {
  .banner img {
    width: 8.875rem;
  }
  .cliped {
    clip-path: polygon(0% 0%, 100% 0, 100% 50%, 40% 50%);
  }
}
</style>
