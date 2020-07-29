<template>
  <view class="index">
      <my-button typeicon="success" typebtn="primary" title="这是成功的tit" ></my-button>
      <picker mode='selector' :range="selector" @change="onchange">
            <view className='picker'>
                当前选择：{{selectorChecked}}
            </view>
    </picker>
  </view>
</template>

<script>
import './index.scss'
import MyButton from '../../components/button';

export default {
    components: {
        MyButton
    },
    data() {
        return {
            selector: ['美国', '中国', '巴西', '日本'],
            selectorChecked: '美国'
        }
    },
    methods: {
        onchange(e) {
            this.selectorChecked = this.selector[e.detail.value]
        }
    }
}
</script>
