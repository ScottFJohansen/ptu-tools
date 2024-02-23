<script>
	import Card from "./Card.svelte";
	import Text from "./Text.svelte";
    import Types from "./Types.svelte";
    import Number from "./Number.svelte";
	import Picklist from "./Picklist.svelte";
</script>

<Card>
    <div class="flex flex-col items-center gap-y-4">
        <h2 class="text-3xl text-center w-full border-b border-b-gray-500">General Info</h2>
        <Text classes="mt-8 w-full" label="Name" name="name"/>
        <div class="flex flex-row w-full justify-between gap-x-4">
            <Text classes="w-3/4" label="Species" name="species"/>
            <Number classes="w-1/4" label="Level" name="level"/>
        </div>
        <div class="flex flex-row w-full justify-between gap-x-4">
            <Types classes="w-full" name="type1" label="Type 1"/>
            <Types noneAllowed classes="w-full" name="type2" label="Type 2"/>
        </div>
        <div class="flex flex-row w-full justify-between gap-x-4">
            <Picklist classes="w-full" name="gender" label="Gender" options={["Male", "Female", "Genderless"]} />
            <Number classes="w-1/2" label="Loyalty" name="loyalty" />
            <Text classes="w-full" label="Held Item" name="held-item"/>
        </div>
        <div class="flex flex-row w-full justify-between gap-x-4">
            <Text classes="w-1/2" label="Weight" name="weight"/>
            <Text classes="w-1/2" label="Height" name="height"/>
        </div>
    </div>
</Card>