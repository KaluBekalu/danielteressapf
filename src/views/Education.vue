<template>
  <div id="education" class="education">
    <h1>Educations</h1>
    <div class="cards">
      <EduCard v-for="edu in educations" :key="edu.id" :info="edu" />
    </div>
  </div>
</template>

<script>
import EduCard from "../components/EduCard.vue";
export default {
  data() {
    return {
      groupNumber: 1,
      maxGroup: 2,
    };
  },
  components: { EduCard },
  props: { educations: { type: Object } },
  methods: {
    nextGroup() {
      if (this.groupNumber < this.maxGroup) this.groupNumber += 1;
      console.log(this.groupNumber);
    },
    prevGroup() {
      if (this.groupNumber > 1) this.groupNumber -= 1;
      console.log(this.groupNumber);
    },
  },
};
</script>

<style scoped>
.education {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-top: 3rem;
  overflow: hidden;
}
.education h1 {
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
