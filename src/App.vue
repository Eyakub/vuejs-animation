<template>
    <div style="margin-top: 200px;">
        <button class="btn btn-primary" @click="show = !show">Toggle</button>
        <transition name="fade">
            <p v-if="show">Hi there its me, Animation</p>
        </transition>
    </div>
</template>

<script>


export default {
    data(){
        return {
            show: false
        };
    }
}
</script>

<style>
.fade-enter, .fade-leave-to{
    opacity: 0;
}

.fade-enter-active, .fade-leave-active{
    transition: opacity 2s;
}
</style>
