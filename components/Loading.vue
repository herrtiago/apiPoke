<template>
  <div class="flex justify-center items-center bg-emerald-300 h-screen w-screen ">
    <div class="loader"></div>
  </div>
</template>

<script>
export default {
  name: "Loading",
};
</script>

<style>
.loader {
    width:2%;
    height: 2%;
  border: 50px solid #030303;
  border-color: #ff3d00 #ff3d00 #fff #fff;
  border-radius: 50%;
  position: relative;
  animation: rotate 1s linear infinite;
}

.loader:before {
  content: "";
  position: absolute;
  top: 50%;
  transform: translate(-50%, -125%);
  left: 50%;
  width: 12px;
  height: 12px;
  border: 2px rgb(2, 2, 2) solid;
  background: #fff;
  border-radius: 50%;
}
@keyframes rotate {
  100% {
    transform: rotate(-360deg);
  }
}
</style>