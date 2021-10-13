<template>

<!-- Select component -->
<div>
    <label class="select-label mb-0">{{ label }}</label>
    <div class="select-box">
        <select>
            <option disabled selected></option>
            <option value="1">United Bank for Africa</option>
            <option value="2">Guaranty Trust Bank</option>
        </select>
    </div>
</div>
</template>

<script>
export default {
    props: {
        label: {
            type: String,
            default: 'Label'
        }
    },
}
</script>

