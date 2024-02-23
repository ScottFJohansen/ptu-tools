<script lang="ts">
    export let value: any = null;
    export let name: string;
    export let type: string;
</script>

<input type="{type}" class="w-3/4 p-2 bg-gray-100 border border-gray-300 active:border-blue-100" name="{name}" id="{name}" value="{value}"/>