<script lang="ts">
    const props: {
        link: string
        title: string
        description: string
        image: string
        imageAlt: string
    } = $props()
</script>

<a href={props.link}
    ><h2>{props.title}</h2>
    <div class="content-container">
        <img src={props.image} alt={props.imageAlt} />
        <p>{props.description}</p>
    </div>
</a>

<style>
    a {
        display: flex;
        flex-direction: column;
        backdrop-filter: grayscale(50%) blur(10px);
        border-radius: 10px;
        border-style: outset;
        border-color: var(--color);
        color: var(--color);
        text-decoration: none;
        border-width: 0px;
        padding: 5px;
    }
    a:hover {
        padding: 0px;
        border-width: 5px;
    }
    h2 {
        margin: 10px;
        margin-bottom: 0px;
        font-size: 1.4rem;
    }
    .content-container {
        display: flex;
        gap: 30px;
        padding: 20px;
    }
    img {
        width: 64px;
        object-fit: contain;
    }
</style>
