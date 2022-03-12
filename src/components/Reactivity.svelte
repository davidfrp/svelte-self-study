<script>
    let weekdays = [
        "Monday",
        "Tuesday",
        "Wednesday",
        "Thursday",
        "Friday",
        "Saturday",
        "Sunday"
    ];

    let randomIndex = 0;
    $: weekday = weekdays[randomIndex];
    
    $: if (weekday === 'Monday') {
        weekday = weekday + ' :(';
    } else if (weekday === 'Friday') {
        weekday = weekday + ' :)';
    }
    
    function handleClick() {
        randomIndex = Math.floor(Math.random() * weekdays.length);
    }
</script>

<button on:click={handleClick}>
    Get another random day of week!
</button>
<p class="pulse">{weekday}</p>

<style>
    @media (prefers-reduced-motion: no-preference) {
        .pulse {
            animation: pulse 2.5s infinite;
        }
    
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
    }
</style>
