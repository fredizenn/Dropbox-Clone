<script lang="ts">
	import * as  Table  from "./ui/table";
    let files = [];
</script>

<div class="border rounded-md my-10 shadow-md">
    <h1 class="py-5 capitalize font-medium pl-5">
        files(5)
    </h1>
    {#if files.length === 0}
        <div class="flex justify-center items-center h-[200px]">
            <p class="text-gray-400">No files uploaded</p>
        </div>
    {:else}
    
    <Table.Root>
        <Table.Caption>A list of your recent invoices.</Table.Caption>
        <Table.Header>
          <Table.Row>
            <Table.Head class="w-[100px]">Type</Table.Head>
            <Table.Head>File Name</Table.Head>
            <Table.Head>File Size</Table.Head>
            <Table.Head>Date Added</Table.Head>
            <Table.Head>Link</Table.Head>
            <Table.Head class="sr-only">Delete</Table.Head>
          </Table.Row>
        </Table.Header>
        <Table.Body>
            {#each {length: 5} as _}
          <Table.Row>
            <Table.Cell class="font-medium">{"INV001"}</Table.Cell>
            <Table.Cell>{"Paid"}</Table.Cell>
            <Table.Cell>{"Credit Card"}</Table.Cell>
            <Table.Cell>{"$250.00"}</Table.Cell>
          </Table.Row>
          {/each}
        </Table.Body>
      </Table.Root>
      {/if}
</div>