<template>
  <div>
    <!-- 1. Beberapa Elemen HTML yang berbeda -->
    <h1>Hello World</h1>
    <hr style="border: 2px solid black">
    <ul>
      <li>Hobi saya adalah olahraga dan sunmori</li>
      <li>Saya Madridistas</li>
    </ul>
    <!-- 2. Elemen input teks -->
    <input type="text" v-model="inputText" placeholder="Ketik disini" />
    <!-- 3. Gabungkan penggunaan class binding dan style binding -->
    <div :class="{ 'spotted': isSpotted }" :style="{ color: textColor, backgroundColor: bgColor }">
      Halo, nama saya Dwi Herza Anugrah
    </div>
    <!-- 4.Interaksi dinamis dengan menggunakan event listeners -->
    <button @click="colorBgText">Click Me</button>
    <p>{{ Text }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
      isSpotted: false,
      textColor: 'green',
      Text: ':)'
    };
  },
  methods: {
    colorBgText() {
      this.Text = ':)';
      this.isSpotted = !this.isSpotted;
    },
  }
};
</script>

<style scoped>
.spotted {
  background-color: skyblue;
}
</style>