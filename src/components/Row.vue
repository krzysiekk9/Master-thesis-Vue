<script>
    import './table.css'
    export default {
        props: ['rowNum']
    }
</script>

<template>
    <tr class="row">
        <td>{{ rowNum }}</td>
        <td>{{ rowNum }}</td>
        <td>{{ rowNum }}</td>
    </tr>
</template>

