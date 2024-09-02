<template>
    <header :class="{ 'scrolled': isScrolled }">
        <nav>
            <!-- Contenido del menú de navegación -->
            <ul>
                <li class="logo">
                    <p>Sebastian tellier</p>
                </li>
                <li><a href="/">Inicio</a></li>
                <li><a href="/about">Acerca de</a></li>
                <li><a href="/contact">Contacto</a></li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data() {
        return {
            isScrolled: false,
        };
    },
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
    },
    beforeUnmount() { // Updated hook
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        handleScroll() {
            this.isScrolled = window.scrollY > 0;
        },
    },
};
</script>

<style scoped>
@import url(https://fonts.googleapis.com/css2?family=Cedarville+Cursive&display=swap);

header {
    position: fixed !important;
    width: 100%;
    backdrop-filter: blur(1px);
    z-index: 1000;
    background-color: rgba(234, 255, 245, 0.757);
    transition: background-color 0.3s ease;
    border-bottom: 1px solid #ccc;
    padding: 10px;

    nav {
        ul {
            display: flex;
            align-items: center;
            /* Alinea verticalmente */
            padding: 5px;
            list-style-type: none;
            margin: 0;
            /* Elimina el margen por defecto del ul */

            li {
                margin: 0 15px;
                /* Espaciado horizontal */

                /* Asegura que el logo no afecte a otros elementos */
                &:not(.logo) {
                    display: flex;
                    align-items: center;
                }

                &.logo {
                    margin-right: auto;
                    /* Empuja el logo a la izquierda */

                    p {
                        font-family: 'Cedarville Cursive', cursive;
                        color: #2f3d50;
                        font-size: 24px;
                        /* Tamaño del texto del logo */
                        margin: 0;
                        /* Elimina el margen por defecto del p */
                        padding: 0;
                        /* Elimina el padding por defecto del p */
                        line-height: 1;
                        /* Ajusta la altura de la línea */
                    }
                }

                a {
                    font-family: sans-serif;
                    border: 1px solid rgba(135, 255, 201, 0.98);
                    font-size: medium;
                    color: #2f3d50;
                    padding: 5px;
                    border-radius: 10px;
                    text-decoration: none;
                    display: flex;
                    /* Asegura que el padding y el tamaño se mantengan constantes */
                    align-items: center;
                    justify-content: center;

                    &:hover {

                        background-color: rgba(135, 255, 201, 0.8);
                    }
                }

            }
        }
    }
}


header.scrolled {


    nav {
        ul {


            li {

                &.logo {

                    color: rgb(0, 199, 73);

                }

            }
        }
    }

    backdrop-filter: blur(4px);
    background-color: rgba(255, 255, 255, 0.773);
    /* Color de fondo cuando se desplaza */
}
</style>
