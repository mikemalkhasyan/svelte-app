<script>
    export let celeb;
</script>

<div class="card-outer">
    <button class="card-inner" style="background-image: url({celeb.image})">
        <div class="details">
            <h2>
                <a target="_blank" href="https://cameo.com/{celeb.id}">{celeb.name}</a>
            </h2>
            <p class="type">{celeb.type}</p>
        </div>
    </button>
</div>

<style>
    .card-outer {
        width: 100%;
        height: 100%;
    }

    .card-inner {
        position: absolute;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        background: 50% 0 no-repeat;
        background-size: cover;
        overflow: hidden;
        padding: 0;
        text-align: center;
    }

    .details {
        position: absolute;
        width: 100%;
        bottom: 0;
        padding: 1em 0.5em 0.5em 0.5em;
        background: linear-gradient(to bottom, transparent, rgba(0,0,0,0.6) 35%, rgba(0,0,0,0.9));
        color: white;
    }

    h2 {
        margin: 0 0 0.2em 0;
    }

    .type {
        margin: 0;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
    }

    @media (min-width: 640px) {
        .card-outer {
            height: 0;
            padding: 0 0 100% 0;

        }
    }
</style>