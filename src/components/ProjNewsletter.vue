<template>
<div class="main-container">
  <div class="container">
    <h3>Subscribe Now to Our Newsletter !</h3>
    <div class="input-container">
      <input placeholder="Email address..." type="text">
      <button class="btn btn-y"><i class="fa-solid fa-paper-plane"></i></button>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'NewsLetterSec'
}
</script>

<style scoped lang="scss">
@import '../assets/styles/partials/_variables.scss';
@import '../assets/styles/partials/_general.scss';

.main-container{
  background-color: $main-red;
  color: white;
  .container{
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 7rem;
    h3{
      font-size: 2rem;
    }
    .input-container{
      width: 30%;
      height: 2.5rem;
      background-color: white;
      border-radius: 1.5rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      &:focus-within{
        outline: 3px solid $main-gold;
      }
      .btn{
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 50%;
        height: 2.7rem;
        width: 2.7rem;
      }
      input{
        border: none;
        outline: none;
        margin-left: 1rem;
      }
    }
  }
}
</style>
