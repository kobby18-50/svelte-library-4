<script>
	import '../app.pcss';
    import { Button } from 'flowbite-svelte'
	import LoginModal from '../components/LoginModal.svelte';
	import FooterComponent from '../components/FooterComponent.svelte';

  let loginModal = false

</script>

<nav class="flex justify-between mx-10 md:mx-12 lg:mx-16 mt-5">
    <div><a href="/">LOGO</a></div>

    <div>
        <Button on:click={() => (loginModal = true)} class='bg-book-primary hover:bg-book-secondary hover:text-book-primary hover:duration-300'> + Upload Book</Button>
    </div>
</nav>

<LoginModal bind:open = {loginModal} />

<slot />

<FooterComponent/>
