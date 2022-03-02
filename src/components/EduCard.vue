<template>
  <div class="edu-card">
    <div class="edu-card-header">
      <h1>{{ info.title }}</h1>
      <span></span>
    </div>
    <div class="edu-card-bottom">
      <ul class="description">
        <li>{{ info.year }}</li>
        <li>{{ info.degree }}</li>
      </ul>
      <ul class="title">
        <li>Year</li>
        <li>Degree</li>
      </ul>
    </div>
    <div class="edu-address">
      <p>{{ info.institution }}</p>
      <p>{{ info.address }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: { info: { type: Object } },
};
</script>

<style>
.edu-card {
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  max-width: 20rem;
  min-width: 20rem;
  height: fit-content;
  align-items: center;
  padding: 3rem 0 6rem 0rem;
  gap: 1.5rem;
  box-shadow: rgb(17 17 26 / 10%) 0px 1px 0px, rgb(17 17 26 / 10%) 0px 8px 24px,
    rgb(17 17 26 / 10%) 0px 16px 48px;
  transition: 500ms ease;
}
.edu-card:hover {
  transform: scale(1.07);
  transition: 500ms ease;
  cursor: default;
}

.edu-card-header {
  height: 3rem;
}
.edu-card-header > h1 {
  font-size: 1.3rem;
  text-align: center;
  height: 3rem;
  display: flex;
  align-items: center;
}

.edu-card-header > span {
  width: 60%;
  height: 1px;
  background: #20273c;
  display: block;
  margin: auto;
  margin-top: 5px;
  border-radius: 50%;
}
.edu-card-bottom {
  display: flex;
  justify-content: center;
  width: 100%;
  gap: 0.8rem;
  font-size: 1.3rem;
  line-height: 2rem;
  margin-top: 1rem;
}
.edu-card-bottom ul {
  list-style: none;
}
.edu-card-bottom span {
  height: 4rem;
  width: 1px;
  background: #000;
}
.edu-card-bottom .title {
  flex: 1;
}
.edu-card-bottom .description {
  text-align: end;
  font-weight: 200;
  flex: 2;
  background: #20273c;
  color: #fff;
  padding-right: 10px;
  box-sizing: border-box;
  border-radius: 0 1rem;
}

.edu-address {
  text-align: end;
  align-self: end;
  margin-right: 2rem;
}
.edu-address p:nth-child(1) {
  font-size: 1.2rem;
}
.edu-address p:nth-child(2) {
  font-size: 1rem;
  font-weight: 300;
  margin-top: 0.3rem;
  color: #002bae;
}
</style>
