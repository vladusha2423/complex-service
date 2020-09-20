<template>
    <div class="clients">
        <div class="clients-title">С кем мы работаем</div>
        <div class="clients-container">
            <div v-for="(card, i) in cards" :key="i" class="clients-card">
                <div class="clients-card-title nav-button">{{ card.title }}</div>
                <img :src="card.icon" :alt="card.title" class="clients-card-icon">
                <div class="clients-card-list">
                    <div v-for="(point, i) in card.list" :key="i" class="clients-card-list-point">
                        <span>&#9658; </span>{{ point }}
                    </div>
                </div>
                <v-btn class="nav-button">Подробнее</v-btn>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Clients",
        data(){
            return {
                cards: [
                    {
                        title: 'Автобусы',
                        icon: require('../../../assets/images/bus-icon.png'),
                        list: [
                            'Организация технического обслуживания ТО',
                            'Ремонт и/или установка нового оборудования',
                            'Устранение мелких неисправностей',
                            'Ремонт электроники',
                            'Прочий сервис'
                        ]
                    },
                    {
                        title: 'Такси',
                        icon: require('../../../assets/images/taxi-icon.png'),
                        list: [
                            'Организация технического обслуживания ТО',
                            'Ремонт и/или установка нового оборудования',
                            'Установка газового оборудования',
                            'Ремонт электроники',
                            'Прочий сервис'
                        ]
                    },
                ]
            }
        }
    }
</script>

<style lang="scss" src="./Clients.scss" scoped/>