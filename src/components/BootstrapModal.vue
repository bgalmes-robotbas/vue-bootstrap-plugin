<template>
<div class="modal fade" :id="idModal" :ref="idModal" tabindex="-1" :aria-labelledby="idModal" aria-hidden="true">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h5 class="modal-title">{{ title }}</h5>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <div class="modal-body">
                <slot name="body"></slot>
            </div>
            <div class="modal-footer">
                <slot name="footer"></slot>
            </div>
        </div>
    </div>
</div>
</template>


<script>
export default {
    name: 'BootstrapModal',
    props: {
        title: {
            required: true,
            type: String
        },
        idModal: {
            required: true,
            type: String
        },
    },

    setup() {
        return {}
    }
}
</script>
