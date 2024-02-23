<script lang="ts">
	import Label from "./Label.svelte";


    export let name: string;
    export let label: string;
    export let options: string[];
    export let classes: string = "";

</script>

<div class="{classes} flex flex-row gap-x-4 items-center">
    <Label name="{name}" label="{label}"/>
    <select class="bg-gray-100 w-3/4 p-2 border border-gray-300" id={name} name={name}>
        {#each options as option}
            <option value={option}>{option}</option>
        {/each}
    </select>
</div>