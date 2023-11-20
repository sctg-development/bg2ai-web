<template>
  <main>
    <div class="wrapper">
      <h1>laser<span class="dot">+</span>smart</h1>
      <p>a new era is coming…</p>
      <div class="logo">
        <img src="https://ismo-group.co.uk/static/logo.svg" />
      </div>
    </div>
  </main>
</template>

<script setup lang="ts">
import { version as Version, ref, onMounted } from 'vue'
const version = ref(Version)
onMounted(() => {
  console.log(`Vue version ${version.value}`)
  document.getElementsByTagName("body")[0].classList.add('homebody');
})
</script>

<style>
.homebody {
  background: #00091B;
  color: #fff;
}
</style>

<style scoped>
@keyframes fadeIn {
  from {
    top: 20%;
    opacity: 0;
  }

  to {
    top: 100;
    opacity: 1;
  }

}

@-webkit-keyframes fadeIn {
  from {
    top: 20%;
    opacity: 0;
  }

  to {
    top: 100;
    opacity: 1;
  }

}

.wrapper {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  -webkit-transform: translate(-50%, -50%);
  animation: fadeIn 1000ms ease;
  -webkit-animation: fadeIn 1000ms ease;

}

h1 {
  font-size: 50px;
  font-family: 'Poppins', sans-serif;
  margin-bottom: 0;
  line-height: 1;
  font-weight: 700;
}

.dot {
  color: #4FEBFE;
}

p {
  text-align: center;
  margin: 18px;
  font-family: 'Muli', sans-serif;
  font-weight: normal;
}


.logo {
  padding: 4em;
}</style>