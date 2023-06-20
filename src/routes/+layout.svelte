<script>
    import '../app.css';
</script>

<nav class="flex justify-center items-center w-full bg-neutral-800 border-slate-200">
    <a href="/" class="font-bold text-3xl text-white">Home</a>
    <a href="/about" class="font-bold text-3xl text-white">About</a>
</nav>
<br><br><br><br>
<div class="p-8 max-w-6xl mx-auto">
    <slot></slot>
</div>

<style>
    a {
        margin: 0 9rem;
        text-decoration: none;
    }
    a:hover {
        color: rgba(196, 196, 196, 0.986);
    }
</style>