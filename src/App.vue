<template>
    <div style="margin-top: 200px;">
        <button class="btn btn-primary" @click="show = !show">Toggle</button>
        <transition>
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
.v-enter, .v-leave-to{
    opacity: 0;
}

.v-enter-active, .v-leave-active{
    transition: opacity 1s;
}
</style>
