<template>
  <head>
    <title>เคยสงสัยไหมว่าคุณใจเกเรรึเปล่านะ?</title>
  </head>
  <div>
    <div class="min-h-screen flex justify-center items-center">
      <div>
        <div class="mb-10">
          <h1 class="text-4xl font-bold text-transparent bg-clip-text bg-gradient-to-br from-orange-300 to-orange-400">
            คุณใจเกเรรึเปล่านะ?
          </h1>
        </div>
        <div class="grid gap-2 mb-5">
          <input v-model="name" type="text" placeholder="ชื่อของคุณ"
            class="bg-white/10 text-white outline-none rounded-md p-2 transition-all hover:scale-105">
          <input v-model="age" type="text" placeholder="อายุของคุณ"
            class="bg-white/10 text-white outline-none rounded-md p-2 transition-all hover:scale-105">
          <input v-model="color" type="text" placeholder="คุณชอบสีอะไร"
            class="bg-white/10 text-white outline-none rounded-md p-2 transition-all hover:scale-105">
          <button @click="check"
            class="bg-gradient-to-br from-orange-300 to-orange-400 text-white font-bold rounded-md p-1.5 transition-all hover:scale-105">ตรวจสอบ</button>
        </div>
        <div class="text-center">
          <span class="text-xl font-bold text-transparent bg-clip-text bg-gradient-to-br from-orange-300 to-orange-400">
            {{ start }}
            <span
              class="text-2xl font-bold text-transparent bg-clip-text bg-gradient-to-br from-purple-300 to-purple-400">
              {{ end }}
            </span>
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const name = ref('');
const age = ref('');
const color = ref('');
const start = ref('');
const end = ref('');

function check() {
  if (name.value !== '' && age.value !== '' && color.value !== '') {
    start.value = `คุณ${name.value} คุณนี่มัน`;
    end.value = `เกย์ตัวพ่อ!`;
  } else {
    start.value = '';
    end.value = '';
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Kanit:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

body {
  font-family: 'Kanit', sans-serif;
  background-color: rgb(39, 33, 29);
  
}
</style>
