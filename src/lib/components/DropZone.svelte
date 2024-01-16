<script lang="ts">

let isDragging = false;
let fileInput: HTMLInputElement;

function handleClick() {
    fileInput.click();
}

function handleDragEnter() {
    isDragging = true;
}

function handleDragLeave() {
    isDragging = false;
}

function handleDrop() {
    isDragging = false;
}
</script>

<div>
    <button
    on:click={handleClick}
    on:dragenter|preventDefault={handleDragEnter}
    on:dragleave|preventDefault={handleDragLeave}
    on:drop|preventDefault={handleDrop}
    class="w-full rounded-lg bg-border/50 h-44 border-4 border-dashed">
        {#if isDragging}
        drop the file here
        {:else}
        drag and drop a file here or click to add files
        {/if}
        <input type="file" bind:this={fileInput} hidden multiple />
    </button>
</div>