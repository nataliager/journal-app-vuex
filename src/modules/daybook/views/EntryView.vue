<template>
    <div class="entry-tittle d-flex justify-content-between p-2">
        <div>
            <span class="text-success fs-3 fw-bold">24</span>
            <span class="mx-1 fs-3">Junio</span>
            <span class="mx-2 fs-4 fw-light">2023, Sabado</span>
        </div>
        <div>
            <button class="btn btn-danger mx-2">
                Borrar
                <i class="fa fa-trash-alt"></i>
            </button>
            <button class="btn btn-primary">
                Subir foto
                <i class="fa fa-upload"></i>
            </button>
        </div>
    </div>
    <hr>
    <div class="d-flex flex-column px-3 h-75">
        <textarea placeholder="que sucedio hoy?"></textarea>
    </div>
    <FabComponent icon="fa-save" />

    <img src="https://www.eltiempo.com/files/article_main_1200/uploads/2023/06/02/647a22bd65efa.jpeg" alt="entry-picture"
        class="img-thumbail">
</template>

<script>
import { defineAsyncComponent } from 'vue'
defineAsyncComponent
export default {
    components: {
        FabComponent: defineAsyncComponent(() => import('../components/FabComponent.vue'))

    }
}
</script>

<style lang="scss" scoped>
textarea {
    font-size: 20px;
    border: none;
    height: 100%;

    &:focus {
        outline: none;
    }
}

img {
    width: 200px;
    position: fixed;
    bottom: 150px;
    right: 20px;
    box-shadow: 0px 5px 10px rgba($color: #000000, $alpha: 0.2);
}
</style>