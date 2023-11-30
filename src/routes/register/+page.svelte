<script>
	import { Label, Input, Button } from "flowbite-svelte";


</script>


<form class="grid mx-5 gap-y-10 md:mx-40">

    <div>
        <Label htmlFor='name'>Name</Label>
        <Input placeholder='Kwabena Okai' name = 'name' id='name' class='focus:ring-0 focus:border-book-primary' />
    </div>

    <div>
        <Label htmlFor='email'>Email</Label>
        <Input placeholder='user@mail.com' name = 'email' id='email' type='email' class='focus:ring-0 focus:border-book-primary' />
    </div>

    <div>
        <Label htmlFor='password'>Password</Label>
        <Input placeholder='••••••••' name = 'password' id='password' class='focus:ring-0 focus:border-book-primary'/>
    </div>

    <Button type='submit' class='bg-book-primary hover:bg-book-secondary hover:duration-300 hover:text-book-primary focus:ring-0'>Register Account</Button>
</form>