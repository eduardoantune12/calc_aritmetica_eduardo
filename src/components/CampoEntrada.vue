<template>
    <div class="form-group">
        <label :for="id">{{ label }}</label>
        <input
            :id="id"
            :type="type"
            class="form-control"
            v-model="value"
        />
    </div>
</template>

<script>
export default {
    props: {
        id: String,
        label: String,
        type: String,
        value: Number
    }
}
</script>