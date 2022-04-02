<template>
<div class="main-container">
  <div class="container">
    <div class="centered p-relative">
      <img style="width: 50px;" src="../assets/img/Clock-and-Bell.png" alt="">
      <h2>University Year</h2>
      <div class="graphic">
        <div style="bottom: -1.4rem; left:-80px; " class="text-container">
          <h4>Orientation</h4>
          <p>First day of university year, all students gather for the opening ceremony and then network with others</p>
        </div>
        <div style="top: 160px; left: 160px" class="text-container">
          <h4>Demo Classes</h4>
          <p>In the first week , students try to accomodate with the teaching style and choose theri optional courses.</p>
        </div>
        <div style="bottom: -1.4rem; right:160px;" class="text-container">
          <h4>Evaluation</h4>
          <p>At the end of a semester, students take a general evaluation test for every subject they're learning.</p>
        </div>
        <div style="top: 160px; right: -60px" class="text-container">
          <h4>Graduation Day</h4>
          <p>On the day of graduation, all students gather for the ceremony and then network and party among others.</p>
        </div>
        <img src="../assets/img/Timeline-Item.png" alt="">
      </div>
    </div>
  </div>
  <div class="centered pb-10 pt-10">
      <img style="width: 50px;" src="../assets/img/upcoming-events-calendar-icon.png" alt="">
      <h2>Upcoming Events</h2>
      <div class="events-container">
        <div class="event p-relative" v-for="ele in arrEvents" :key="ele.type">
          <h3>{{ele.type}}</h3>
          <p><i class="fa-regular fa-calendar"></i> {{ele.date}}</p>
          <p>{{ele.descripion}}</p>
          <button class="btn-r btn"><i class="fa-solid fa-plus"></i> {{ele.textBtn}}</button>
        </div>
      </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'MainSec3',
  data () {
    return {
      arrEvents: [
        {
          type: 'Coaching Sesion',
          date: '20 May 21.30',
          descripion: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.Lorem ipsum [...]',
          textBtn: 'Find More'
        },
        {
          type: 'Coaching Sesion',
          date: '24 Mar 18.00',
          descripion: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.Lorem ipsum [...]',
          textBtn: 'Find More'
        },
        {
          type: 'Coaching Sesion',
          date: '12 Feb 13.30',
          descripion: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.Lorem ipsum [...]',
          textBtn: 'Find More'
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../assets/styles/partials/_variables.scss';
@import '../assets/styles/partials/_general.scss';

.main-container{
  background-color: $main-red;
  color: white;
  .container{
    height: 500px;
  }
  .centered{
    height: 100%;
  }
}
.text-container{
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 45%;
  p{
    width: 90%;
    margin: .4rem;
  }
}
.graphic{
  img{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%)
  }
}
.text-container{
  position: absolute;
}
.events-container{
  display: flex;
  p{
    width: 80%;
  }
  .event{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 1rem;
    border-radius: 1rem;
    height: 200px;
    width: 300px;
    background-color: white;
    color: $text-blue;
    box-shadow: 0px 1px 5px rgba($color: #000000, $alpha: 0.3);
    h3{
      font-size: 1.6rem;
    }
    p{
      color: #8b8b8a;
      font-size: 0.8rem;
      margin: .3rem;
    }
    .btn{
      padding: .5rem 1rem;
      position: absolute;
      bottom: -1rem;
      box-shadow: 0px 1px 5px rgba($color: #000000, $alpha: 0.3)
    }
  }
}

</style>
