<template>
    <div id="teasers">
        <div class="teasers">
            <div v-for="(teaser, i) in teasers" :key="i" class="teasers-point">
                <img class="teasers-point-icon" :src="teaser.icon" :alt="teaser.title">
                <div class="teasers-point-title">{{ teaser.title }}</div>
                <div class="teasers-point-text">{{ teaser.text }}</div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Teasers",
        data(){
            return {
                teasers: [
                    {
                        title: 'Гарантия качества',
                        text: 'У нас работают только квалифицированные специалисты',
                        icon: require('../../../assets/images/teaser1.svg'),
                    },
                    {
                        title: 'Широкий профиль',
                        text: 'Выбирайте самые разные услуги - от ремонта двигателя до замены стекол',
                        icon: require('../../../assets/images/teaser2.svg'),
                    },
                    {
                        title: 'Оперативность',
                        text: 'Придем на помощь в кратчайшие сроки',
                        icon: require('../../../assets/images/teaser3.svg'),
                    },
                    {
                        title: 'Честность',
                        text: 'Рассчитываем цену в соответствии с запросом, делая ваш счет таким, какой он должен быть на самом деле',
                        icon: require('../../../assets/images/teaser4.svg'),
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" src="./Teasers.scss" scoped/>