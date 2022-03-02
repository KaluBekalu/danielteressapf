<template>
  <div id="certifications" class="certifications">
    <h1>{{ "Certifications & Awards" }}</h1>
    <div class="cards">
      <CertCard v-for="cert in certifications" :key="cert.id" :cert="cert" />
    </div>
  </div>
</template>

<script>
import CertCard from "../components/CertCard.vue";
export default {
  data() {
    return {
      groupNumber: 1,
      maxGroup: 2,
    };
  },
  components: { CertCard },
  props: { certifications: { type: Object } },
};
</script>

<style scoped>
.certifications {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-top: 3rem;
  overflow: hidden;
  padding: 2rem 0;
  background: #13293e;
  color: #fff;
}
.certifications h1 {
  text-align: center;
}

.cards {
  width: 90%;
  display: flex;
  gap: 2rem;
  padding: 3rem 2rem;
  margin-inline: auto;
  margin-top: 0.5rem;
  position: relative;
  justify-content: space-between;
  max-width: 80rem;
}

.active {
  display: flex;
}
.btnNext {
  right: 0;
}
.btnNext,
.btnPrev {
  position: absolute;
  font-size: 2rem;
  background: #a0a0ac;
  width: 3rem;
  border-radius: 50%;
  height: 3rem;
  top: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  box-sizing: border-box;
}

.btnNext:hover,
.btnPrev:hover {
  transform: translateX(-2px) scale(1.1);
}
</style>
