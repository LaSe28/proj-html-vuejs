<template>
<div class=" p-relative">
  <div class="pb-10 container">
    <div class="centered mt-2 pt-5">
      <h1>Key to your success</h1>
      <p class="mb-2 mt-2">EduPrime is the most versatile WordPress THeme for educational purposes, showcasing universities, courses, secondary schools etc.</p>
      <div>
        <button class="mt-1 mr-1 btn btn-y"><i class="fa-solid fa-magnifying-glass"></i> Search courses</button>
        <button class="mt-1 btn btn-w"><i class="fa-solid fa-user-plus"></i> Apply for university</button>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'MainSec1'

}
</script>

<style scoped lang="scss">
@import '../assets/styles/partials/_general.scss';
@import '../assets/styles/partials/_variables.scss';

h1{
  font-size: 3rem;
  font-weight: bold;
}
.btn-y:hover{
  background-color: white;
  color: $main-red;
}
.btn-w:hover{
  background-color: $main-gold;
  color: white;
}

</style>
