<template>
  <div id="contact" class="contact">
    <div class="contact-header">
      <h1>Contact</h1>
    </div>
    <div class="detail">
      <div class="contact-detail">
        <div class="left">
          <p>Email</p>
          <p>Phone</p>
          <p>LinkedIn</p>
          <p>Twitter</p>
        </div>
        <span class="divider"></span>
        <div class="right">
          <p>{{ personalInfo.email }}</p>
          <p>{{ personalInfo.mobile }}</p>
          <p>
            <a
              target="_blank"
              href="https://www.linkedin.com/in/daniel-teressa-62907181/"
              >Daniel Teressa</a
            >
          </p>
          <p>
            <a target="_blank" href="https://twitter.com/danielteress"
              >Daniel Teressa</a
            >
          </p>
        </div>
      </div>
      <img src="../assets/image2.jpg" alt="" />
    </div>
  </div>
</template>

<script>
export default {
  props: { personalInfo: { type: Object } },
};
</script>

<style>
.contact {
  display: flex;
  flex-direction: column;
  margin-block: 3rem;
}
.detail {
  flex-direction: column-reverse;
  position: relative;
  display: flex;
  align-items: center;
  margin: auto;
  margin-top: 3rem;
  justify-content: space-evenly;
}
.detail img {
  width: 10rem;
  border: 2px solid #ffffff30;
  object-fit: cover;
  zoom: 1;
  box-shadow: rgb(17 17 26 / 10%) 0px 1px 0px, rgb(17 17 26 / 10%) 0px 8px 24px,
    rgb(17 17 26 / 10%) 0px 16px 48px;
  border-radius: 50%;
}
.contact h1 {
  text-align: center;
  font-size: 2rem;
}
.contact-detail {
  position: inherit;
  display: flex;
  gap: 1.5rem;
  padding: 1rem;
  margin-block: 4rem;
  border: 1px solid;
  font-size: 1.5rem;
  border-inline: none;
}
.left p,
.right p {
  margin-bottom: 10px;
}
.left {
  text-align: end;
  font-weight: 200;
}
.right {
  text-align: start;
}
.right a {
  text-decoration: none;
  color: black;
  transition: 500ms ease-in-out;
}
.right a:hover {
  background: #13293e;
  color: #fff;
  /* padding-left: 5px; */
  padding: 5px;
  border-radius: 5px;
  transition: 500ms ease-in-out;
}

.divider {
  width: 1px;
  height: 15rem;
  background: black;
  position: absolute;
  left: 25%;
  bottom: -2rem;
}

@media (max-width: 800px) {
  .contact-detail {
    font-size: 1rem;
  }
  .divider {
    height: 13rem;
  }
}
</style>
