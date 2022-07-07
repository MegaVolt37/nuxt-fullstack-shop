<template>
  <div class="Header">
    <ul>
      <li>
        <nuxt-link to="/">Домой</nuxt-link>
        <a href="/second" @click.prevent="$router.push('/second')">На базу</a>
        <a href="/about" @click.prevent="goToAbout">туда его</a>
        <nuxt-link to="/first">Ага</nuxt-link>
        <nuxt-link to="/abouts">Зачем</nuxt-link>
      </li>
    </ul>
    <button @click="plus">click</button>
  </div>
</template>
<script setup>

const router = useRoute();
let page = 1;
function plus() {
  page++;
  console.log(page);
}
function goToAbout() {
  const rout = useRoute();
  rout.push("/about");
  console.log(rout);
}
</script>
<style>
.Header {
  position: absolute;
  bottom: 0;
}
</style>
