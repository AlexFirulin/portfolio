<template>
  <input
    type="checkbox"
    :checked="colorMode.preference === 'dark'"
    @change="toggleMode"
    class="form-toggle"
  />
</template>

<script setup>

const colorMode = useColorMode()

const toggleMode = () => {
  colorMode.preference = colorMode.preference === 'light' ? 'dark' : 'light'
}
</script>

<style scoped>
.form-toggle {
  position: relative;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  width: 40px;
  height: 20px;
  background: #ccc;
  outline: none;
  border-radius: 20px;
  box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.2);
  transition: background 0.3s;
  cursor: pointer;
}

.form-toggle:checked {
  background: #0c190c;
}

.form-toggle::before {
  content: '';
  position: absolute;
  left: 0;
  width: 50%;
  height: 100%;
  background: rgb(27, 89, 127);
  border-radius: 50%;
  transition: transform 0.3s;
}

.form-toggle:checked::before {
  transform: translateX(100%);
}
</style>
