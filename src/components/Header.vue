<script setup>
    const props = defineProps({
        titreHeader: {
            type: String,
            required: true
        }
    })    
</script>

<template>
    <header>
        <h2>{{titreHeader}}</h2>
        <nav>
           <ul>
            <li>
                <a href="/">Accueil</a>
            </li>
            <li>
                <a href="/about">A propos</a>
            </li>
           </ul>
        </nav>
    </header>
</template>

<style lang="scss" scoped>
    header {
        
        width: 100%;
        display: flex;
        justify-content: space-between;
        @media screen and (min-width: 768px) {
            max-width: 1240px;
            width: 100%;
            margin: 30px auto;
        }

        nav {
            display: block;
            ul {
                display: flex;
                gap: 15px;
                list-style: none;
                li {
                    margin-left: 1rem;
                }
            }
        }
    }
</style>
