<script lang="ts">
	import Input from "./Input.svelte";
	import Label from "./Label.svelte";

    export let label: string;
    export let value: string = "";
    export let name: string;
    export let classes: string = "";
</script>

<div class="{classes} flex flex-row gap-x-4 items-center">
    <Label label={label} name={name}/>
    <Input type="text" name="{name}" value="{value}"/>
</div>