<script>
	import Card from "$lib/Card.svelte";

</script>
<div class="pt-12 flex flex-col items-center w-full gap-y-12">
    <div class="flex flex-col items-center gap-y-4">
        <h1 class="text-5xl"><strong>Welcome!</strong></h1>
        <p class="text-gray-900">
                Try navigating the site with the links below!
        </p>
    </div>
    <div class="flex flex-row w-full px-8 gap-x-12 justify-center">
        <div class="w-1/3">
            <Card>
                <div class="flex flex-col items-center">
                    <h1 class="text-3xl text-center w-full border-b border-b-gray-500"><strong>Pokémon</strong></h1>
                    <p class="mt-4 text-center">
                        Here you can create Character sheets for your Pokémon. It will calculate stats, base relations and more to make your life as easy as possible.
                        Includes saving functionality to generate a JSON output that you can use to restore the data back into the form.
                    </p>
                    <a href="/pokemon">
                        <button class="mt-4 text-white rounded-lg bg-green-500 px-4 py-2 border border-gray-600 hover:bg-green-600">
                            Create a Pokémon >>
                        </button>
                    </a>
                </div>
            </Card>
        </div>
        <div class="w-1/3">
            <Card>
                <div class="flex flex-col items-center">
                    <h1 class="text-3xl text-center w-full border-b border-b-gray-500"><strong>Trainer</strong></h1>
                    <p class="mt-4 text-center">
                        Here you can create Character sheets for your Trainers. Provides lots of space for you to take notes during a session
                        and stores all of your stats, features and edges. Includes saving functionality to generate a JSON output that you can 
                        use to restore the data back into the form.
                    </p>
                    <a href="/trainer">
                        <button class="mt-4 text-white rounded-lg bg-red-500 px-4 py-2 border border-gray-600 hover:bg-red-600">
                            Create a Trainer >>
                        </button>
                    </a>
                </div>
            </Card>
        </div>
    </div>
    <div class="w-1/3">
        <Card>
            <div class="flex flex-col items-center">
                <h1 class="text-3xl text-center w-full border-b border-b-gray-500"><strong>How To Use</strong></h1>
                <p class="mt-4 text-center">
                    Explanation of how the application works and advice on how to use it during a session/campaign.
                </p>
                <a href="/help">
                    <button class="mt-4 text-white rounded-lg bg-blue-500 px-4 py-2 border border-gray-600 hover:bg-blue-600">
                        How To Use >>
                    </button>
                </a>
            </div>
        </Card>
    </div>
</div>