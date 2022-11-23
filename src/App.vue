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
  <Transition name="slide-up">
    <div class="back-top" @click="scrollToTop()" v-show="isTop"><i class="fa-solid fa-arrow-up"></i></div>
  </Transition>
</template>

<script>
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';

  export default {
    data(){
      return{
        show: false,
        isTop: false
      }
    },
    methods: {
        scrollToTop() {
            window.scrollTo(0, 0);
        },
    },
    mounted(){
        const that = this
        window.addEventListener('scroll', () => {
            let scrollPos = window.scrollY
            if(scrollPos >= 100){
                that.isTop = true
            } else {
                that.isTop = false
            }
        })
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
    background-color: #163eaa;
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

.back-top{
  z-index: 600;
  position: fixed;
  bottom: 30px;
  right: 100px;
  width: 35px;
  height: 35px;
  line-height: 35px;
  text-align: center;
  background-color: white;
  border-radius: 50%;
  border: 1px solid black;
  cursor: pointer;
  transition: 0.2s;
  &:hover{
    background-color: rgb(42, 42, 42);
    color: white;
  }
}
.slide-up-enter-active {
        transition: all 0.5s ease-out;
    }

    .slide-up-leave-active {
        transition: all 0.5s cubic-bezier(1, 0.5, 0.8, 1);
    }

    .slide-up-enter-from,
    .slide-up-leave-to {
        transform: translateY(50px);
        opacity: 0;
    }
</style>