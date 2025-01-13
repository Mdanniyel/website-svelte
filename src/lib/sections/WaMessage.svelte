<script>
    let { text } = $props();
    let src = "wa-background.png"
</script>

<div class="py-4">
    <div class="flex items-center justify-center p-2 rounded-lg" style="background-image: url({src}); background-color: #eae6df;">
        <div class="flex justify-start">
            <div
                class="relative max-w-xl rounded-lg bg-white px-3 py-2 text-gray-800 shadow"
            >
                <p class="text-xl">
                    {text}
                </p>
            </div>
        </div>
    </div>
</div>

<style>
</style>
