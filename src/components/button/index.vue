<template>

  <view class="index">
    <text>{{ title }}</text>
    <icon size='20' :type='typeicon' v-if="typeicon"></icon>
    <button @tap="onTap" size='mini' :type='typebtn'>{{title}}</button>

  </view>
</template>

<script>


export default {
    props: {
        title: '',
        typebtn: '',
        typeicon: ''
    },
    methods: {
        onTap() {
            console.log(this.title);
        }
    }
}
</script>
