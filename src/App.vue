<template>
  <HeaderComponent />
  <MainComponent />
  <FooterComponent />
  <Transition name="slide-fade">
    <div class="chat" v-show="show">
      <h4 class="text-white text-center pt-4 pb-2">Send a message to our team</h4>
      <div class="inner-chat">
        <div class="message">Hi, How can I help you?</div>
        <input type="text" class="input" placeholder="Send a message">
      </div>
    </div>
  </Transition>
  <div class="chat-icon" @click="show = !show"><i class="fa-regular fa-comment"></i></div>
</template>

<script>
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';

  export default {
    data(){
      return{
        show: false
      }
    },
    components: { HeaderComponent, MainComponent, FooterComponent }
}
</script>

<style lang="scss" scoped>
@use './assets/variables' as *;
@use './assets/mixins' as *;

.chat-icon{
  z-index: 600;
  position: fixed;
  bottom: 10px;
  right: 20px;
  background-color: $bg-turchese;
  width: 60px;
  height: 60px;
  line-height: 60px;
  font-size: 2rem;
  text-align: center;
  border-radius: 50%;
  color: $white;
  cursor: pointer;
  &:hover{
    background-color: #3159c9;
  }
  }
  .chat{
    z-index: 600;
    position: fixed;
    bottom: 75px;
    right: 20px;
    height: 85vh;
    width: 350px;
    border-radius: 0.5rem;
    background: linear-gradient(180deg, $bg-turchese 35%, white 35%);
    border: 1px solid black;
    .inner-chat{
      width: 90%;
      height: 85%;
      margin: auto;
      display: flex;
      align-items: flex-start;
      flex-wrap: wrap;
    }
    .message{
      margin-top: 3rem;
      padding: 1rem;
      width: max-content;
      border-radius: 0.5rem;
      background-color: #D5F9BA;
    }
    .input{
      width: 100%;
      font-size: 1.3rem;
      align-self: flex-end;
    }
  }
  .slide-fade-enter-active {
        transition: all 0.5s ease-out;
    }

    .slide-fade-leave-active {
        transition: all 0.5s cubic-bezier(1, 0.5, 0.8, 1);
    }

    .slide-fade-enter-from,
    .slide-fade-leave-to {
        transform: translateY(-50px);
        opacity: 0;
    }
</style>