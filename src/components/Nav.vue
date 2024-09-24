<template>
    <nav>
        <div id="logo">Marco Lazzari</div>
        
        <ul class="links">
            <li><a href="">About</a></li>
            <li><a href="">Experience</a></li>
            <li><a href="">Projects</a></li>
            <li><a href="">Contact</a></li>
        </ul>
    </nav>
</template>

<style>
    nav{
        display: flex;
        justify-content: space-around;
        align-items: center;
        height: 15vh;
    }

    #logo{
        font-size: 2rem;
    }

    nav .links{
        list-style: none;
        display: flex;
        gap: 1rem;
        font-size: 1.5rem;
    }
</style>