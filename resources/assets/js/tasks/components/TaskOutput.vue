<template>
    <span>
        <button class="uk-button uk-button-link" @click="showModal = true">
            <span uk-icon="icon: more"></span>
        </button>
        <uikit-modal :show="showModal" @close="showModal = false">
            <div class="uk-modal-header">
                <h3>Output</h3>
            </div>
            <div class="uk-modal-body uk-overflow-auto uk-height-max-large">
                <div v-html="output"></div>
            </div>
            <div class="uk-modal-footer">
                <div class="uk-flex uk-flex-right">
                    <button class="uk-button uk-button-small uk-button-primary" @click="showModal = false">Close</button>
                </div>
            </div>
        </uikit-modal>
    </span>
</template>
<script>
    import UIKitModal from '../../components/UIKitModal.vue'
    export default {
        name: 'TaskOutput',
        components: {
            'uikit-modal':UIKitModal
        },
        props: {
            output: {
                type: String
            }
        },
        data() {
            return {
                showModal: false,
            };
        }
    }
</script>
