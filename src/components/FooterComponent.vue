<template>
    <footer class="footer">
       
    </footer>
</template>

<script>
export default {
    name: 'FooterComponent'
}
</script>

<style scoped>
.footer {
    background: #2f373c;
    padding: 40px;
    color: aliceblue;
}

.footer-content {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
}

.footer-links {
    list-style: none;
    padding: 0;
    margin: 0;
}

.footer-links li {
    margin-bottom: 10px;
}

.footer-links a {
    text-decoration: none;
    color: aliceblue;
}

.footer-info {
    font-size: 0.9em;
}

.footer-info p {
    margin: 0;
    margin-bottom: 10px;
}
</style>
