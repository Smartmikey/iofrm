<script>
    import "../app.css";
    import { page, navigating } from '$app/stores';

    // @ts-ignore
    // const { params: {path} } = $page;
    console.log($page.params);
    console.log($page.route);
    console.log($page.url.pathname);
</script>

<div class="container">
    <div class="layout-bg">
        <img src="/img2.jpg" class="layout-bg-img" alt="background" />
            <img src="/logo-dark.svg" class="logo-desktop" alt="" />
    </div>


    <div class="form-section-container">
        <div>
            <img src="/logo.svg" class="logo-mobile" alt="" />
            <h3 class=" font-bold text-2xl my-2">Get more things done with Loggin platform.
            </h3>
            <p class="font-thin leading-6 mb-3">Access to the most powerfull tool in the entire design and web industry.</p>

            <ul class="flex space-x-6 font-thin">
                <li class={`py-2 ${$page.url.pathname === '/login' || $page.url.pathname === '/' ? 'font-bold border-b-2': 'border-b '}`}><a href="/login">Login</a></li>
                <li class={`py-2 ${$page.url.pathname === '/register' ? 'font-bold border-b-2': 'border-b '}`}><a href="/register">Register</a></li>
            </ul>
            <slot />

        </div>
    </div>
</div>