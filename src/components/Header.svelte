<script>
    export let y;

    export let tabs = [
        { name: "Projects ", link: "#projects" },
        { name: "About Me", link: "#about" },
        { name: "Blog", link: "https://www.youtube.com/watch?v=dQw4w9WgXcQ" },
        // { name: "Contact", link: "" },
        // {name: '', link: ''},
    ];
</script>

<header
    class={"sticky z-[10] top-0 duration-500 px-6 flex items-center justify-between border-b border-solid " +
        (y > 0
            ? " py-4 bg-transparent border-white"
            : " py-6 bg-transparent border-transparent")}
>
    <h1 class="font-medium">
        <b class="font-bold poppins">Zedaes</b> 
    </h1>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="duration-500 hover:text-green-400"
                target={index === 2 ? "_blank" : ""}
            >
                <p>{tab.name}</p>
            </a>
        {/each}
        <!-- <button
            class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-green-600 text-white"
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-green-400 opacity-20 group-hover:translate-x-full z-0 duration-100"
            />
            <h4 class="relative z-9">Login</h4>
        </button> -->
        <button
            class="greenShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-green-950"
        >
            <div
                class="absolute top-0 right-full w-full h-full bg-green-400 opacity-20 group-hover:translate-x-full z-0 duration-500"
            />
            <h4 class="relative z-9">Get in touch</h4>
        </button>
    </div>
</header>