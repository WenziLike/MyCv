<template>
    <div class="modal-backdrop" @click="$emit('close')"></div>
    <div class="modal">
        <h3>Certificates</h3>
        <button class="btn">Load Certificates</button>
        <input
          type="file"
          id="file"
          :accept="accept"
          ref="file"
          :multiple="multiple"
          @change="getfile"
        />
    </div>
</template>

<script>
export default {
    emits: ['close'],
    inject: ['modal'],
    data() {
        return {
            multiple: true,
            accept: [...['.png', '.jpg', '.jpeg', '.gif']],
            file: null,
        }
    },
    mounted() {
    },
    methods: {
        greateButton(tag, classes = [], content) {
            const node = document.createElement(tag)

            if (classes.length) {
                node.classList.add(...classes)
            }
            if (content) {
                node.textContent = content
            }
        },
        getfile() {
            // this.file = this.$refs.file.files[0]
            console.log(this.$refs.file.files[0])
        },
    },
}
</script>

<style lang="scss" scoped>
body {
    .modal {
        background: rgba(0, 0, 0, 0.432);
        color: #fff;
        .btn {
            position: relative;
            text-align: center;
            left: 0;
            &:active {
                box-shadow: -3px -3px 4px #ffffff73,
                2px 2px 2px rgba(94, 104, 121, 0.288);
                color: #2c3e50;
                text-align: left;
            }
        }
        input[type="file"] {
            display: none;
        }
    }
}
</style>