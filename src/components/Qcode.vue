<template>
    <div class="main">
        <div>
            <input type="text" v-model="text"><button @click="makeCode(text)">生成二维码</button>
        </div>
        <div style="width: 132px;height: 132px">
            <div id="qrcode"></div> <!-- 创建一个div，并设置id为qrcode -->
        </div>
    </div>
</template>

<script>
    import QRCode from 'qrcodejs2'  // 引入qrcode
    export default {
        name : 'Qcode',
        data () {
            return {
                text: 'http://www.baidu.com',
                codeObj: null
            }
        },
        mounted () {
            this.qrcode();
        },
        methods: {
            qrcode() {
                this.codeObj = new QRCode('qrcode', {
                    width: 132,
                    height: 132,
                    colorDark : "#000",
                    colorLight : "#fff",
                })
            },
            makeCode (text) {
                this.codeObj.makeCode(text)
            }
        }
    }
</script>

<style scoped>
 .main{
     display: flex;
     flex-direction: column;
 }
</style>
