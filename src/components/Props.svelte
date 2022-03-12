<script>
    export let name;
    export let age;
    export let avatar;
</script>

<div class="profile">
    <img src={avatar} alt="">
    <div class="profile-info">
        <h2>{name}</h2>
        <p>{age} years old</p>
    </div>
</div>

<style>
    .profile {
        margin-top: 2.5rem;
        display: inline-flex;
        align-items: center;
        gap: 1rem;
    }

    @media (prefers-reduced-motion: no-preference) {
        .profile:hover img {
            animation: spin 0.25s linear infinite;
        }

        @keyframes spin {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }
    }

    .profile-info {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
    }

    .profile-info * {
        margin: 0;
    }

    img {
        width: 55px;
        height: 55px;
        border-radius: 50%;
        object-fit: cover;
    }
</style>
