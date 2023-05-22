<script setup lang="ts">
</script>

<template>
  <div class="main-bg">
    <div class="wrapper">
      <div class="menu">
        <span class="title-letter">H
          <div class="menu-item">Hello</div>
        </span>
        <span class="title-letter">A
          <div class="menu-item">Are you familiar with wine?</div>
        </span>
        <span class="title-letter">R
          <div class="menu-item">Reservation</div>
        </span>
        <span class="title-letter">A
          <div class="menu-item second-letter">mArriage</div>
        </span>
        <span class="title-letter">G</span>
        <span class="title-letter">O</span>
        <span class="title-letter">G</span>
        <span class="title-letter">I</span>
        <span class="title-letter">P</span>
        <span class="title-letter">E</span>
      </div> 
    </div>
  </div>
</template>
<style lang="scss" scoped>
  .main-bg {
    width: 100vw;
    height: 100vh;
    text-align: center;
    border: 1px solid;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-image: url("../assets/img/bg2.jpg");
    background-repeat : no-repeat;
    background-size : 80%;
    background-position: center;
    overflow-y: hidden;
    overflow-x: hidden;
    .wrapper {
      width: 120vw;
      transform: rotate(-30deg);
      font-size: 5.5em;
      letter-spacing: 1.5em;
      .menu {
        animation-duration: 6s;
        animation-name: slidein;
        .title-letter {
          font-weight: 100;
          display: inline-block;
          transform: rotate(30deg);
          text-shadow: 4.5px 2px 2px #a9a9a9;
          .menu-item {
            display: none;
            position: absolute;
            top: 0;
            text-align: left;
            letter-spacing: 0.2em;
            
            animation: move .5s;
            white-space: nowrap;
          }
          .second-letter {
            left: -1.13em;
            animation: move2 .5s;
          }
        }
        .title-letter:hover {
          cursor: pointer;
          .menu-item {
            display: block;
            border-bottom: 1px solid;
          }
        }
      }
    }
/** animation part */    
    @keyframes slidein {
      from {
        margin-left: 100%;
        width: 100%
      }
      to {
        margin-left: 0%;
        width: 100%;
      }
    }
    @keyframes move {
      from { left: 25vw; opacity: 0; }
      30% { opacity: 0; }
      50% { opacity: 0.2; }
      70% { opacity: 0.3; }
      to { left: 0; opacity: 0.4; }
    }
    @keyframes move2 {
      from { left: 25vw; opacity: 0; }
      30% { opacity: 0; }
      50% { opacity: 0.2; }
      70% { opacity: 0.3; }
      to { left: -1.13em; opacity: 0.4; }
    }
  }
</style>