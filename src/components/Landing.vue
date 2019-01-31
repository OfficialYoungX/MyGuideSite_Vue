<template>
  <div class="page">
    <div class="avatar__container">
        <div class="avatar"></div>
    </div>
    <div class="yo">
      <p>
        <span class="yo__qing">welcome</span>
        <span class="yo__orange">to my</span>
        <span class="yo__puple">site</span>
      </p>
      <div class="arrow-left"></div>
      <p>
        <span class="yo__deep-orange">decode</span>
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../scss/animation.scss';

$standard-time: 4s;
$animation: $standard-time ease infinite alternate;

span{
    display: inline-block;
}

.page {
  flex-shrink: 0;
  width: 100vw;
  height: 100vh;
  background-color: black;
  display: grid;
  grid-template-columns: 2fr 3fr;
  justify-items: center;
  align-items: center;
}

$avatar-size: 10rem;
.avatar__container{
    width: $avatar-size + 2rem;
    height: $avatar-size + 2rem;
    border-radius: 50%;
    border: 0.3rem solid $deep-orange;
    display: flex;
    justify-content: center;
    align-items: center;
    box-shadow: 0 0 3vw $deep-orange;
    
}
.avatar{
    width: $avatar-size;
    height: $avatar-size;
    border-radius: 50%;
    background-image: url(../assets/avatar.jpg);
    background-position: center;
    background-size: cover;
}

.yo{
    text-align: center;
    cursor: default;
}

.yo__qing ,.yo__orange, .yo__puple, .yo__deep-orange{
    font-weight: 800;
    font-size: 3rem;
    margin: 0 1rem;
}

.yo__qing{
    color: $qing;
    text-shadow: 0 0 3vw $qing;
    animation: neon-qing  $animation;
    @include neon-qing($qing, $qing-neibor, $qing-neibor-darken);
}
.yo__orange{
    color: $orange;
    text-shadow: 0 0 3vw $orange;
    animation: neon-orange $animation;
    @include neon-orange($orange, $orange-neibor, $orange-neibor-darken);
}
.yo__puple{
    color: $puple;
    text-shadow: 0 0 3vw $puple;
    animation: neon-puple $animation;
    @include neon-puple($puple, $puple-neibor, $puple-neibor-darken);
}
.yo__deep-orange{
    color: $deep-orange;
    text-shadow: 0 0 3vw $deep-orange;
    animation: neon-deep-orange $animation;
    @include neon-deep-orange($deep-orange, $deep-orange-neibor, $deep-orange-neibor-darken);
}

.arrow-left{
    width: 36rem;
    height: 3rem;
    background-image: url(../assets/arrow-right.png);
    background-position: center;
    background-size: cover;
}
</style>