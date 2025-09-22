<script lang="ts">
    import GitHub from './assets/github.png'
    import LinkedIn from './assets/linkedin.png'
    import ProjectDisplay from './ProjectDisplay.svelte'
    import Reddit from './assets/reddit.png'
    import Svelte from './assets/svelte.png'
</script>

<main>
    <h1>pritoranta</h1>
    <p>
        Professional software developer and architect. Intrigued about how
        software can serve and delight people. I like building simple things
        that spark joy. Here's a little collection of fun stuff I made! 💝
    </p>
    <p class="italic">I feel like I'm back at the Green Dragon.</p>
    <div id="project-container">
        <ProjectDisplay
            title="Reddit Gallery Client"
            link="https://pritoranta.net/reddit-gallery-client/"
            description="Svelte browser app made for browsing pictures on Reddit in a unique way. Draws a grid where some pictures are enlarged based on a semi-random chance. Meant to be used on a desktop monitor for the proper 'wow' effect. Click to see..."
            image={Reddit}
        />
        <ProjectDisplay
            title="Reddit Gallery API"
            link="https://github.com/pritoranta/reddit-gallery-api/"
            description="Backend service for Reddit Gallery Client. Web API written in Go, powered by the Gin framework. Fetches data from Reddit API and caches it. If subject to too frequent unique requests (across all users), Reddit API will start rate limiting it. More on GitHub..."
            image={Reddit}
        />
        <ProjectDisplay
            title="Portfolio"
            link="https://github.com/pritoranta/portfolio/"
            description="What you're looking at right now! Super simple Svelte browser app written in TypeScript, and compiled into HTML + CSS + JavaScript. As simple as it gets. No server components."
            image={Svelte}
        />
    </div>
    <div id="socials">
        <a href="https://github.com/pritoranta" target="_blank"
            ><img src={GitHub} /></a
        >
        <a
            href="https://linkedin.com/in/pietari-ritoranta-b9895a203"
            target="_blank"><img src={LinkedIn} /></a
        >
    </div>
</main>

<style>
    main {
        display: flex;
        gap: 20px;
        flex-direction: column;
        align-items: center;
        padding: 1rem;
    }
    h1 {
        font-size: 2.5rem;
        margin: 0;
    }
    #project-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 10px;
        width: 100%;
    }
    p {
        text-align: center;
        padding-left: 15%;
        padding-right: 15%;
    }
    .italic {
        text-shadow: 1px 1px 1px var(--color);
        font-style: italic;
    }
    #socials {
        display: flex;
        gap: 20px;
        justify-content: flex-end;
        width: 100%;
    }
    #socials a img {
        height: 64px;
    }
</style>
