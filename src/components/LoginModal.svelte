<script>
	import { Checkbox, Label, Modal, Input, Button } from "flowbite-svelte";

    export let open = false


</script>

<Modal bind:open={open} size="xs" autoclose={false} class="w-full">
    <form class="flex flex-col space-y-6" action="#">
      <h3 class="mb-4 text-xl font-medium text-gray-900 dark:text-white">Sign in to upload your book</h3>
      <Label class="space-y-2">
        <span>Email</span>
        <Input type="email" name="email" placeholder="name@mail.com" required />
      </Label>
      <Label class="space-y-2">
        <span>Your password</span>
        <Input type="password" name="password" placeholder="••••••••" required />
      </Label>
      <div class="flex items-start">
        <Checkbox>Remember me</Checkbox>
        <a href="/" class="ml-auto text-sm text-book-primary hover:underline"> Lost password? </a>
      </div>
      <Button type="submit" on:click={() =>(open = false)} class="w-full1 bg-book-primary hover:bg-book-secondary focus:ring-0 focus:border-0 hover:duration-300">Login to your account</Button>
      <div class="text-sm font-medium text-gray-500 dark:text-gray-300">
        Not registered? <a href="/register" on:click={() =>(open = false)} class="text-book-primary hover:underline"> Create account </a>
      </div>
    </form>
  </Modal>