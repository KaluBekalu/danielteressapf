<template>
  <div class="exp-card">
    <div class="header">
      <div v-if="exp.current" class="top">
        <p>Current Position</p>
      </div>

      <h1>
        <span>{{ exp.role.split(" ")[0] }}</span
        >{{ exp.role.split(" ").slice(1).join(" ") }}
      </h1>
    </div>
    <span></span>
    <div class="bottom">
      <p class="organization">{{ exp.institution }}</p>
      <div class="date">
        <p class="from">{{ exp["start-date"] }}</p>
        <span>-</span>
        <p class="to">{{ exp["end-date"] }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: { exp: { type: Object } },
};
</script>

<style scoped>
.header {
  min-height: 10rem;
  display: flex;
  align-items: end;
}
.exp-card {
  color: #13293e;
  background: #fff;
  position: relative;
  display: flex;
  flex-direction: column;
  width: max-content;
  row-gap: 1rem;
  padding: 2rem;
  border-radius: 10px;
  box-shadow: rgb(17 17 26 / 10%) 0px 1px 0px, rgb(17 17 26 / 10%) 0px 8px 24px,
    rgb(17 17 26 / 10%) 0px 16px 48px;
  transition: 500ms ease;
}
.exp-card:hover {
  transform: scale(1.07);
  transition: 500ms ease;
  cursor: default;
}

.top {
  position: absolute;
  width: 100%;
  height: 3rem;
  bottom: 100%;
  right: 0;
  opacity: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.6rem;
  font-weight: 300;
  color: #fff;
  background: #13293e;
  border-radius: 10px 10px 0 0;
  border: 1px solid #fff;
  box-sizing: border-box;
}

.exp-card:hover .top {
  top: 0%;
  opacity: 1;
}
.exp-card:hover h1,
.exp-card:hover .date {
  background: #13293e;
  color: #fff;
  padding-left: 5px;
  padding-right: 15px;
  transition: 500ms ease-in-out;
}

.exp-card > span {
  background: #13293e;
  width: 100%;
  height: 2px;
}
.exp-card h1 span {
  font-weight: 200;
  margin-right: 10px;
}
.exp-card h1 {
  display: flex;
  flex-direction: column;
  grid-column-start: 1;
  grid-column-end: 3;
  margin-top: 2rem;
  margin-bottom: 0.4rem;
  width: fit-content;
  font-size: 1.6rem;
  border-radius: 0.2rem;
  transition: 500ms ease-in-out;
}

.bottom {
  display: flex;
  flex-direction: column;
  height: 7rem;
  justify-content: space-between;
}

.exp-card .organization {
  margin-right: 1.3rem;
  margin-bottom: 2rem;
}
.exp-card .date {
  display: flex;
  gap: 6px;
  font-weight: 300;
  letter-spacing: 2px;
  height: fit-content;
  white-space: nowrap;
  padding: 5px;
  border-radius: 0.2rem;
  transition: 500ms ease-in-out;
}
</style>
