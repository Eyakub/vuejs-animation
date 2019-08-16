<template>
    <div style="margin-top: 200px;">
        <button class="btn btn-primary" @click="show = !show">Toggle</button>
        <transition 
            enter-active-class="animated pulse slow"

            leave-active-class="animated zoomOut slow">
            <p v-if="show" style="width: 200px;">Hi there its me, Animation</p>
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
    .slow{
        animation-duration: 3s;
    }
</style>
