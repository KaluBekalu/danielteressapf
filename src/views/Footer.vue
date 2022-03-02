<template>
  <footer>
    <div class="copyright">
      Daniel Teressa {{ "   ©  " + new Date().getFullYear() }}
    </div>
    <div class="dev">
      <p>Built by</p>
      <a class="devlink" target="_blank" href="https://kalbekalu.netlify.app/"
        >Kalkidan Bekalu <i class="fa-solid fa-arrow-right-long"></i
      ></a>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style>
footer {
  position: relative;
  background: #13293e;
  height: 4rem;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #fff;
  font-size: 1.2rem;
  text-align: center;
  font-weight: 200;
}

.devlink {
  text-decoration: none;
  color: #fff;
  padding-inline: 10px;
  padding-block: 5px;
  box-sizing: border-box;
  border-radius: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border: 1px solid #ffffff40;
  transition: 500ms ease;
}
.devlink:hover {
  background: #fff;
  font-weight: 600;
  color: #13293e;
  transition: 500ms ease;
}

.dev {
  position: absolute;
  right: 1rem;
  display: flex;
  justify-content: space-around;
  align-items: center;
  gap: 5px;
  margin-left: 1rem;
  transition: 500ms ease;
}
</style>
