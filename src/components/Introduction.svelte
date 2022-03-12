<script>
    let name = 'Heather';
    let src = '/images/eye.jpg';
    let dangerousText = '<mark>This</mark> is marked!';
</script>

<h1>Hi! I'm {name}.</h1>
<img {src} alt="An eye with an orange star.">
<p>{@html dangerousText}</p>

<style>
    img {
        max-height: 150px;
        max-width: 100%;
    }
</style>
