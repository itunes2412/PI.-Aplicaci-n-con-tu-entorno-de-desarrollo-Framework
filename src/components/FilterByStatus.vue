<template>
  <div class="filter">
    <div class="item" @click="filter('')">
        PERSONAJES
    </div>
    <div class="item" @click="filter('Alive')">
        VIVOS
    </div>
    <div class="item" @click="filter('Dead')">
        MUERTOS
    </div>
    <div class="item" @click="filter('unknown')">
        DESCONOCIDOS
    </div>
  </div>
</template>

<script >
import { useStore } from 'vuex';

export default{
    setup(){
        const store=useStore()
        const filter=((status)=>{
            store.dispatch('filterByStatus',status)
        })
        return{
            filter
        }
    }
}

</script>

<style lang="scss">
.filter{
    width: 600px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(4,1fr);
    border-radius: 8px;
    overflow: hidden;
    .item{
        padding: 1rem 0.5rem;
        background-color: var(--background-card);
        text-align: center;
        cursor: pointer;
        &:hover{
            color: var(--text-orange);
        }   
    }
}
</style>