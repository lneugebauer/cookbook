<template>
    <NcModal :title="title" @close="$close(false)">
        <div class="modal__wrapper">
            <div class="modal__content">{{ content }}</div>
            <div class="modal__button-bar">
                <NcButton @click="$close(false)">{{
                    t("cookbook", "Cancel")
                }}</NcButton>
                <NcButton type="primary" @click="$close(true)">{{
                    t("cookbook", "OK")
                }}</NcButton>
            </div>
        </div>
    </NcModal>
</template>

<script>
import NcModal from "@nextcloud/vue/dist/Components/NcModal"
import NcButton from "@nextcloud/vue/dist/Components/NcButton"

export default {
    name: "SimpleConfirmModal",
    components: {
        NcModal,
        NcButton,
    },
}
</script>

<style scoped>
.modal__wrapper {
    display: flex;
    flex-direction: column;
    padding: 25px;
    gap: 25px;
}

.modal__content {
    text-align: center;
}

.modal__button-bar {
    display: flex;
    justify-content: flex-end;
    gap: 15px;
}
</style>
