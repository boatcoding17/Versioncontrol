<template>
  <q-page class="flex flex-center column">
    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-vertical.svg"
      style="width: 200px; height: 200px"
    >

    <h1>Hello Quasar!</h1>
    <p>
      This is a starter project for Quasar Framework v2.
      <br />
      To get started, edit <code>src/pages/IndexPage.vue</code>.
    </p>

    <h1>HELLO in template</h1>
    <p>HELLO in template</p>
    <p>HELLO in template</p>
    <p>HELLO in template</p> 

    <!-- Input สำหรับใส่ตัวเลข -->
    <q-input v-model.number="num" type="number" label="กรอกตัวเลข" class="q-mb-md" />

    <!-- ปุ่มกด -->
    <q-btn label="ตรวจสอบคู่/คี่" color="primary" @click="checkEvenOdd" />

    <!-- แสดงผล -->
    <p v-if="result">ผลลัพธ์: {{ result }}</p>
  </q-page>
</template>

<script setup>
import { ref } from 'vue'

const num = ref(null)     // เก็บค่าที่กรอก
const result = ref("")    // เก็บผลลัพธ์

function checkEvenOdd() {
  if (num.value === null) {
    result.value = "กรุณากรอกตัวเลขก่อน"
  } else if (num.value % 2 === 0) {
    result.value = `${num.value} เป็นเลขคู่`
  } else {
    result.value = `${num.value} เป็นเลขคี่`
  }
}
<h1>HELLO 111112344567/h1>
</script>



