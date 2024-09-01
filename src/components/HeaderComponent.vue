<template>
    <header>
        <nav>
            <!-- Contenido del menú de navegación -->
            <ul>
                <li><a href="/">Inicio</a></li>
                <li><a href="/about">Acerca de</a></li>
                <li><a href="/contact">Contacto</a></li>
            </ul>
        </nav>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent', // El nombre del componente
    // data() {
    //     return {
    //         // Define los datos del componente aquí
    //         isLoggedIn: false, // Ejemplo de dato
    //     };
    // },
    // methods: {
    //     // Define métodos aquí
    //     toggleLogin() {
    //         this.isLoggedIn = !this.isLoggedIn;
    //     },
    // },
    // mounted() {
    //     // Lógica para ejecutar cuando el componente se monte
    //     console.log('Header component mounted.');
    // },
};
</script>

<style scoped>
header {
    border: dashed;
    width: 100%;
    background-color: #f5f5f5;

    nav {
        ul {
            display: flex;
            flex-direction: row;
            justify-content: space-around;
            padding: 10px;
            list-style-type: none;

            li {
                a {
                    text-decoration: none;
                    color: #333;
                }
            }
        }
    }
}
</style>