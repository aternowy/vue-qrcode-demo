<template>
    <img
        v-if=qrcode
        :src=qrcode
    />
</template>

<script>
import QRCode from 'qrcode';

    export default {
        name: "QrCode",
        props: {
            url: {
                type: String,
                default: ''
            }
        },
        data() {
          return {
              qrcode: null
          }
        },
        watch: {
            url: function(val) {
                QRCode.toDataURL(val)
                    .then(image => {
                        this.qrcode = image;
                    });
            }
        }
    }
</script>

<style scoped>

</style>