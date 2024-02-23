<script>
	import Card from "$lib/Card.svelte";
	import GeneralInfoCard from "$lib/GeneralInfoCard.svelte";


</script>

<div class="pt-8 flex flex-col items-center gap-y-4">
    <h1 class="text-5xl"><strong>Pokémon</strong></h1>
    <div class="flex flex-row gap-x-8 w-full justify-center px-8">
        <div class="w-1/2">
            <GeneralInfoCard/>
        </div>
        <div class="w-1/2">
            <Card>
                <div class="flex flex-col items-center">
                    <h2 class="text-3xl text-center w-full border-b border-b-gray-500">Stats</h2>
                    Name, Level, Species, Gender (Picklist), Loyalty, Held Item, Held Item Description, Type 1, Type 2, Weight, Height
                </div>
            </Card>
        </div>
    </div>
</div>