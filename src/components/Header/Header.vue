<template>
    <v-carousel hide-delimiters
                class="banner"
                :height="height">
        <v-carousel-item
                v-for="(item,i) in items"
                :key="i"
                :src="item.src"
        >
        <div class="banner-container">
            <div class="banner-content">
                <div class="banner-content-title">{{item.title}}</div>
                <div class="banner-content-text">{{item.text}}</div>
                <v-btn class="nav-button">Подробнее</v-btn>
            </div>
        </div>
        </v-carousel-item>
    </v-carousel>
</template>

<script>
    export default {
        name: "Header",
        data () {
            return {
                width: Number,
                items: [
                    {
                        src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
                        title: 'Отличное решение',
                        text: 'Предоставим Вам услуги по техническому обслуживанию и ремонту автобусов и такси в кратчайшие сроки. Быстро, профессионально, недорого!',
                    },
                    {
                        src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
                        title: 'Гарантия качества',
                        text: 'У нас проходит техосмотр каждый пятый автопарк. Сервис успешно работает в сфере комплексного сервисного обслуживания частных клиентов, а именно с автобусными парками и такси, с 2010-го года. Для вас будут трудиться механики, инженеры и токари нашего сервиса.',
                    },
                    {
                        src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
                        title: 'Делаем здесь и сейчас',
                        text: 'Не тратьте ваше драгоценное время на поиск специалистов. Установить оборудование, организовать своевременный техосмотр, устранить мельчайшие неполадки - эти и другие услуги доступны для заказа на нашем сайте!',
                    },
                ],
            }
        },
        computed: {
            height: function(){
                if(this.width > 820)
                    return window.innerHeight - 120;
                else
                    return 400;
            }
        },
        methods: {
            updateWidth: function(){
                this.width = window.innerWidth;
            }
        },
        created(){
            this.width = window.innerWidth;
            window.addEventListener('resize', this.updateWidth);
        }
    }
</script>

<style lang="scss" src="./Header.scss" scoped/>