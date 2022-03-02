<template>
  <div class="cert-card">
    <div class="cert-card-header">
      <h1>{{ cert.title }}</h1>
      <span></span>
    </div>
    <div class="cert-card-bottom">
      <ul class="title">
        <li>Date</li>
      </ul>
      <ul class="description">
        <li>{{ cert.year }}</li>
      </ul>
    </div>
    <div class="cert-address">
      <p>{{ cert.institution }}</p>
      <p>{{ cert.address }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: { cert: { type: Object } },
};
</script>

<style>
.cert-card {
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  max-width: 20rem;
  min-width: 20rem;
  align-items: center;
  padding: 3rem 1px 2rem 0rem;
  gap: 1.5rem;
  background: #fff;
  color: #20273c;
  box-shadow: rgb(17 17 26 / 10%) 0px 1px 0px, rgb(17 17 26 / 10%) 0px 8px 24px,
    rgb(17 17 26 / 10%) 0px 16px 48px;
  transition: 500ms ease;
}
.cert-card:hover {
  transform: scale(1.07);
  transition: 500ms ease;
  cursor: default;
}

.cert-card-header {
  height: 3rem;
}
.cert-card-header > h1 {
  font-size: 1.3rem;
  text-align: center;
  height: 3rem;
  display: flex;
  align-items: center;
  width: 90%;
  margin-inline: auto;
}

.cert-card-header > span {
  width: 100%;
  height: 2px;
  background: #20273c;
  display: block;
  margin: auto;
  margin-top: 20px;
  border-radius: 50%;
}
.cert-card-bottom {
  display: flex;
  justify-content: center;
  width: 100%;
  gap: 0.8rem;
  font-size: 1.3rem;
  line-height: 2rem;
  margin-top: 1rem;
}
.cert-card-bottom ul {
  list-style: none;
}
.cert-card-bottom span {
  height: 4rem;
  width: 1px;
  background: #000;
}
.cert-card-bottom .title {
  flex: 1;
  text-align: right;
}
.cert-card-bottom .description {
  text-align: left;
  padding-left: 10px;
  font-weight: 200;
  flex: 2;
  background: #20273c;
  color: #fff;
  box-sizing: border-box;
}

.cert-address {
  text-align: end;
  align-self: end;
  margin-right: 10px;
  margin-top: 20px;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}
.cert-address p:nth-child(1) {
  font-size: 1.2rem;
  margin-left: 2px;
}
.cert-address p:nth-child(2) {
  font-size: 1rem;
  font-weight: 300;
  margin-top: 0.3rem;
  color: #002bae;
}
</style>
