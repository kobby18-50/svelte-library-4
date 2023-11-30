<script>
	import { Card, Search, TabItem, Tabs } from 'flowbite-svelte';
	import { nanoid } from 'nanoid';
  import BOOKIMG from '../assets/sample.jpg'

	const categories = [
		{
			id: nanoid(),
			title: 'All Categories'
		},
		{
			id: nanoid(),
			title: 'Fiction'
		},
		{
			id: nanoid(),
			title: 'History'
		},
		{
			id: nanoid(),
			title: 'Technology'
		},
		{
			id: nanoid(),
			title: 'Folktales'
		},
		{
			id: nanoid(),
			title: 'Science'
		},
		{
			id: nanoid(),
			title: 'Africa Culture'
		},
		{
			id: nanoid(),
			title: 'poems'
		},
	];

</script>

<form action="">
	<div class="mx-10 md:mx-20 mt-5">
		<Search placeholder="Search by book title" class="focus:ring-0 focus:border-book-secondary"
		></Search>
	</div>
</form>

<div class="mt-5">
	<!-- categories -->
	<Tabs
		divider={false}
		style="underline"
		class="flex justify-between"
		activeClasses="text-book-primary p-4"
	>
		{#each categories as {title, id} (id) }
    <TabItem
    {title}
    activeClasses="text-book-primary p-4 border-b border-book-primary"
  />
    {/each}
		
	</Tabs>
</div>

<!-- books -->

<section class="mx-10 md:mx-20">
  <div class="w-40 h-60 bg-[url('https://images.pexels.com/photos/3747279/pexels-photo-3747279.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1')] bg-cover bg-no-repeat flex flex-col">
    <p>title</p>
    <p>Body</p>
    <p class="justify-end">Footer</p>
   </div>
</section>
