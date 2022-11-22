<template>
    <div class="bg-blue">
        <footer class="my-container">
            <div class="my-list">
                <img src="img/logotype-2-139x23.png" alt="">
                <ul class="d-flex m-0 p-0">
                    <li v-for="(el,i) in navbar" :key="i"><a :href="el.url" class="links">{{el.title}}</a></li>
                </ul>
                <div class="icons">
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-linkedin"></i>
                    <i class="fa-brands fa-facebook"></i>
                    <i class="fa-brands fa-twitter"></i>
                </div>
            </div>
            <div class="copyright">
                <div>
                    <div>Terms of use</div>
                    <div>Privacy Environmental Policy</div>
                </div>
                <div>Copyright © 2022 Phlox Consulting. All Rights Reserved.</div>
            </div>
        </footer>
    </div>
</template>

<script>
import { navbar } from '../data/store'; 
    export default {
        data(){
            return{
                navbar
            }
        }
    }
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;

footer{
    .my-list{
        border-bottom: 2px solid $text-grey;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 5rem 0;
        .links{
            padding: 0 1rem;
            color: $text-grey;
            text-transform: uppercase;
            font-size: 1.1rem;
            &:hover{
                    color: $bg-red-button;
                }
        }
        .icons{
            color: $white;
            *{
                padding: 0 0.5rem;
                cursor: pointer;
                font-size: 1.2rem;
                &:hover{
                    color: $bg-red-button;
                }
            }
        }
    }
    .copyright{
        display: flex;
        align-items: center;
        justify-content: space-between;
        color: $text-grey;
        padding: 2rem 0;
    }
}
</style>