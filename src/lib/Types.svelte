<script lang="ts">
	import Label from "./Label.svelte";
    type option = {
        value: string,
        color: string
    };

    export let name: string;
    export let label: string;
    export let classes: string = "";
    export let noneAllowed: boolean = false;
    let selectedOption: string;
    let options: option[] = [
    {
        "value": "Normal",
        "color": "#A8A77A"
    },
    {
        "value": "Fire",
        "color": "#EE8130"
    },
    {
        "value": "Water",
        "color": "#6390F0"
    },
    {
        "value": "Electric",
        "color": "#F7D02C"
    },
    {
        "value": "Grass",
        "color": "#7AC74C"
    },
    {
        "value": "Ice",
        "color": "#96D9D6"
    },
    {
        "value": "Fighting",
        "color": "#C22E28"
    },
    {
        "value": "Poison",
        "color": "#A33EA1"
    },
    {
        "value": "Ground",
        "color": "#E2BF65"
    },
    {
        "value": "Flying",
        "color": "#A98FF3"
    },
    {
        "value": "Psychic",
        "color": "#F95587"
    },
    {
        "value": "Bug",
        "color": "#A6B91A"
    },
    {
        "value": "Rock",
        "color": "#B6A136"
    },
    {
        "value": "Ghost",
        "color": "#735797"
    },
    {
        "value": "Dragon",
        "color": "#6F35FC"
    },
    {
        "value": "Dark",
        "color": "#705746"
    },
    {
        "value": "Steel",
        "color": "#B7B7CE"
    },
    {
        "value": "Fairy",
        "color": "#D685AD"
    },
    ]

    $: if (selectedOption) {
        const select = document.getElementById(name);
        if (select) {
            const color = options.find(option => option.value === selectedOption)?.color;
            console.log(color);
            if (color !== undefined){
                select.style.color = color;
            }
            else {
                select.style.color = "black";
            }
        }
    }


</script>

<div class="{classes} flex flex-row gap-x-4 items-center">
    <Label name="{name}" label="{label}"/>
    <select bind:value={selectedOption} class="bg-gray-100 w-3/4 p-2 border border-gray-300" id={name} name={name}>
        {#if noneAllowed}
            <option style="color: black" value="None">None</option>
        {/if}
        {#each options as option}
            <option style="color: {option.color}" value={option.value}>{option.value}</option>
        {/each}
    </select>
</div>
