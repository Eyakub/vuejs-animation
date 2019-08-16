<template>
    <div style="margin-top: 200px;">
        <button class="btn btn-primary" @click="show = !show">Toggle</button>
        <transition>
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
    .v-enter-active{
        animation: pulse 1s;
    }

    .v-leave-active{
        animation: fade-out 1s;
    }

    @keyframes fade-out {
        /* initial state */
        from{
            opacity: 1;
            transition: opacity;
        }
        /* end state */
        to {
            opacity: 0;
        }
    }

    @keyframes pulse{
        from {
            transform: scale3d(1, 1, 1);
        }
        50%{
            transform: scale3d(1.2, 1.2, 1.2);
        }
        to{
            transform: scale3d(1, 1, 1);
        }
    }
</style>
