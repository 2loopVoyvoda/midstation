<template>
    <footer>
        <div class="footer__container">
            <div class="footer__logo">
                <v-btn
                    icon
                    color="#FFFFFF"
                    href="https://discord.gg/QdQ3nStxFn"
                >
                    <v-icon size="30">
                        mdi-discord
                    </v-icon>
                </v-btn>
                <v-btn
                    icon
                    color="#FFFFFF"
                    href="https://twitter.com/2loopVoyvoda"
                >
                    <v-icon size="30">
                        mdi-twitter
                    </v-icon>
                </v-btn>
                <v-btn
                    icon
                    color="#FFFFFF"
                    href="https://www.instagram.com/leninkedin.js/"
                >
                    <v-icon size="30">
                        mdi-instagram
                    </v-icon>
                </v-btn>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    computed: {
        version() {
            return require('../../../package.json').version;
        },
    },
};
</script>

<style lang="scss">
footer {
    background: #7fad94;
    .footer__container {
        padding: 0.5rem 0;
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        justify-items: center;
        align-items: center;
        p, a {
            color: #484848;
        }
        a {
            font-weight: bold;
        }      
    }
    .footer__logo{        
        display: grid;
        grid-template-columns: repeat(4, minmax(36px, 1fr));
        justify-items: center;
        column-gap: 1.5rem;
    }
}

@media (max-width: 430px) {
    footer .footer__container div.licence{
        display: none;
    }
}
</style>
