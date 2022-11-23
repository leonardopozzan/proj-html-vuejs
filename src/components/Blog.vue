<template>
    <section class="bg-blue">
        <div class="my-container">
            <div class="pb-4 title-section">
                <div class="d-flex align-items-center">
                    <div class="line"></div>
                    <div class="sub-title">blog</div>
                </div>
                <div class="d-flex align-items-center justify-content-between">
                    <div class="title">the recent news you must read it</div>
                    <ButtonComponent text="view all" bgColor="#ffc318" bgColorHover="#F00E2E" />
                </div>
            </div>
            <div class="row cards">
                <div class="col-6 my-card">
                    <div class="img-box"><img src="img/startup-business-people-and-strategy-board-PAJ3P9K-1390x1042.jpg" alt=""></div>
                    <div class="info">
                        <div><a href="#" class="link bord-end pe-4">july 4, 2019</a><a href="#" class=" ps-4 link">by paul</a></div>
                        <div class="title">Canadian Consulting Firm acquired by UK Giant </div> 
                        <div class="overview">When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a ...</div>
                    </div>
                </div>
                <div class="col-6 my-card">
                    <div class="img-box"><img src="img/business-people-working-together-on-project-and-5FHSKBL-1390.jpg" alt=""></div>
                    <div class="info">
                        <div><a href="#" class="link bord-end pe-4">july 4, 2019</a><a href="#" class=" ps-4 link">by paul</a></div>
                        <div class="title">Canadian Consulting Firm acquired by UK Giant </div> 
                        <div class="overview">When, while lovely valley teems with vapour around meand eridian sun strikes the upper impenetrable foliage of my trees, and but a ...</div>
                    </div>
                </div>
            </div>
        </div>
    </section>


</template>

<script>
import ButtonComponent from './ButtonComponent.vue';

    export default {
    components: { ButtonComponent }
}
</script>

<style lang="scss" scoped>
@use '../assets/variables' as *;
@use '../assets/mixins' as *;
section{
    .title-section{
        .line{
        width: 50px;
        background-color: $bg-acqua;
        height: 0.2rem;
        margin-right: 1rem;
        }
        .sub-title{
            text-transform: uppercase;
            color: $white;
        }
        .title{
            @include myTitle();
            line-height: 3rem;
            padding: 1rem 0;
        }
    }
    
    .cards{
        padding-bottom: 15rem;
        .my-card{
            position: relative;
            .img-box{
                overflow: hidden;
            }
            img{
                transition: 0.5s;
            }
            &:hover img{
                transform: scale(1.1);
            }
            &:hover .info{
                transform: translateY(20px);
                background-color: $bg-acqua;
            }
            .info{
                position: absolute;
                right: 12px; bottom: -80px;
                z-index: 100;
                width: 75%;
                padding: 3rem 5rem;
                background-color: $white;
                transition: 0.5s;
                .bord-end{
                    border-right: 1px solid $white;
                }
                .link{
                    color: $bg-red-button;
                    font-size: 1.2rem;
                    font-weight: 500;
                }
                .title{
                    font-size: 1.5rem;
                    font-weight: 600;
                    padding: 1rem 0;
                }
                .overview{
                    font-size: 1.1rem;
                    color: $text-light-grey;
                }
            }
        }
    }
}
</style>