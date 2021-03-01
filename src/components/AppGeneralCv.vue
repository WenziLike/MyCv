<template>
    <div class="wrapper-content">
        <h1 class="wrapper-title">{{ firstName }} {{ lastName }}</h1>
        <div class="flex-sa">
            <div class="card">
                <div class="card shadow-drop-2-center">
                    <div class="wrapper-logo">
                        <strong>{{ logo }}</strong>
                    </div>
                    <div class="circle-image">
                        <img src="./../assets/my.jpg" class="my-foto" alt="my-foto">
                    </div>
                    <div class="card-contacts">
                        <ul>
                            <li v-for="item in contacts" :key="item">
                                <a :href="item.href">{{ item.text }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="card-adress">
                        <p v-for="item in adress" :key="item">
                            {{ item }}
                        </p>
                    </div>
                </div>
                <app-general-all-skills></app-general-all-skills>
            </div>
            <app-general-content></app-general-content>
        </div>
        <div class="footer card br-5">
            <strong v-html="copy"></strong>
            <strong>VMurakhin, 2021</strong>
        </div>
    </div>
</template>

<script>
import AppGeneralContent from '@/components/AppGeneralContent'
import AppGeneralAllSkills from '@/components/AppGeneralAllSkills'

export default {
    inject: ['logo', 'copy', 'firstName', 'lastName', 'contacts', 'adress'],
    components: {
        AppGeneralContent,
        AppGeneralAllSkills
    }
}
</script>

<style lang="scss" scoped>
#app {
    //.circle-image {
    //    width: 300px;
    //    height: 300px; /* Ширина и высота */
    //    border-radius: 50%; /* Превращаем в круг */
    //    //background: url("./../assets/myfoto.jpg") no-repeat -50px 0; /* Параметры фона */
    //    //background-size: auto 400px; /* Высота фотографии равна высоте элемента */
    //    box-shadow: 2px 6px 12px rgba(0, 0, 0, 0.2);
    //}
    //.my-foto {
    //    display: inline-block;
    //    vertical-align: middle;
    //    width: 300px;
    //    height: 300px; /* Ширина и высота */
    //    border-radius: 50%; /* Превращаем в круг */
    //}

    .circle-image{
        display: inline-block;
        border-radius: 50%;
        overflow: hidden;
        width: 300px;
        height: 300px;
        box-shadow: 2px 6px 12px rgba(0, 0, 0, 0.3);
    }
    .circle-image img{
        width:100%;
        height:100%;
        object-fit: cover;
        transform: rotate(30deg);
    }
}
</style>
