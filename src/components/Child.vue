<template>
    <div>
        <h2>child子组件部分</h2>
        <p>{{message}}</p>
        <button v-on:click="sendMsgToParent">向父组件传值</button>
    </div>
</template>
<script>
    export default {
      props: {
        message: {
            type: String,
            require: true,
        }
      },
      methods: {
        sendMsgToParent () {
            this.$emit('listenToChildEvent','this message id from child')
        }
      }
    }
</script>