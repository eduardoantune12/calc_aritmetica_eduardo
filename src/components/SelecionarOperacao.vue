<template>
    <div class="form-group">
        <label :for="id">{{ label }}</label>
        <select
            :id="id"
            class="form-control"
            v-model="value"
        >
            <option value="+">Soma</option>
            <option value="-">Subtração</option>
            <option value="*">Multiplicação</option>
            <option value="/">Divisão</option>
        </select>
    </div>
</template>

<script>
export default {
    props: {
        id: String,
        label: String,
        value: String
    }
}
</script>