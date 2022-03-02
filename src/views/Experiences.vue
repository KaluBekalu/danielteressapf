<template>
  <div id="experiences" class="experiances">
    <h1>Experiences</h1>
    <div class="cards">
      <ExpCard v-for="exp in experiences" :key="exp.id" :exp="exp" />
    </div>
  </div>
</template>

<script>
import ExpCard from "../components/ExpCard.vue";

export default {
  components: {
    ExpCard,
  },
  props: {
    experiences: { type: Object },
  },
};
</script>

<style>

.experiances {
  background: #13293e;
  color: #fff;
  padding: 2rem;
}
.experiances > h1 {
  text-align: center;
}

.cards {
  display: flex;
  gap: 2rem;
  overflow-x: scroll;
  padding: 2rem;
}


/* width */
::-webkit-scrollbar {
  width: 10px;
  height: 15px;
  position: absolute;
}

/* Track */
::-webkit-scrollbar-track {
  background: #fff;
  border-radius: 20px;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #13293e;
  border: 1px solid #fff;
  border-radius: 20px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #204466;
}
</style>
