<script>
/* 
    Come faccio ad utilizzare un componente dentro un altro?
    Si seguono 3 passaggi:
    1) Importazione del componente
    2) Dichiarazione del componente all'interno dell'oggetto
    3) Utilizzo del componente
*/
// 1) Importazione
import AppHeader from "./components/AppHeader.vue";

export default {
    data() {
        return {
            count: 0,
        };
    },
    // 2) Dichiarazione dei componenti
    components: {
        AppHeader,
    },
};
</script>

<template>
    <a href="#">
        Test fuori
    </a>

    <div id="main">
        <!-- 3) Utilizzo del componente -->
        <AppHeader />

        <h1>Ciao ragazzi</h1>
        <p>
            {{ count }}
        </p>
        <button @click="count++">Incrementa count</button>

        <a href="#">
            Test dentro e diretto

            <button>
                Test
            </button>
        </a>

        <div>
            <a href="#">
                Test dentro e NON diretto

                <button>
                    Test due
                </button>
            </a>
        </div>
    </div>

    <ul>
        <li>
            Ciao 1
        </li>
        <li>
            Ciao 2
        </li>
        <li>
            Ciao 3
        </li>
        <li class="special-li">
            Ciao 4
        </li>
        <li>
            Ciao 5
        </li>
        <li>
            Ciao 6
        </li>
    </ul>
</template>

<style lang="scss" scoped>
@use "assets/scss/main" as *;
</style>
