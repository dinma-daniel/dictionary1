<template>
  <div class="nav__bar">
    <div class="left">
      <a href="https://dribbble.com/dinmadaniel">
        <i class="fab fa-dribbble"></i>
      </a>
      <a href="">
        <i class="far fa-envelope" @click="generateMail()"></i>
      </a>
    </div>

    <div class="right">
      <h2>Use any of these icon links to reach me</h2>
      <h3>Note: Every content was created by me</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Nav',
  methods: {
    generateMail() {
      alert('send mail to ddunebari@gmail.com, thank you')
    },
  },
}
</script>

<style scoped>
:root {
  --color1: #313131;
  --color2: #414141;
  --color3: #525252;
  --color4: #ec625f;
}

.nav__bar {
  /* border: 1px solid red; */
  display: flex;
  justify-content: space-between;
  margin: 4rem;
  width: 28%;
  min-width: 650px;
}

.left {
  display: flex;
  justify-content: space-between;
  align-items: center;
  /* border: 1px solid red; */
  padding: 1.8rem 5rem;
  border-radius: 10px;
  background-color: #414141;
}

i {
  color: white;
  /* border: 1px solid red; */
}

.fab {
  margin-right: 2rem;
  transition: 0.7s;
}

.fab:hover {
  color: violet;
}

.far {
  flex: 0.5;
  margin-left: 2rem;
}

.right {
  display: flex;
  flex-direction: column;
  /* border: 1px solid red; */
  justify-content: center;
  font-size: 0.8rem;
  color: white;
}

h3,
h2 {
  margin: 0;
  padding: 0;
}

h2 {
  font-weight: 500;
}

h3 {
  font-weight: 300;
}

@media (max-width: 900px) {
  .nav__bar {
    flex-direction: column;
    min-width: 80%;
    margin-left: 3rem;
  }

  .right {
    margin-top: 2rem;
  }
}
</style>
