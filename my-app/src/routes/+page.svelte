<script>
    import NavHome from "$lib/components/nav/NavHome.svelte";
    import Button from "$lib/components/Buttons/Button.svelte";
    import KeyArea from "$lib/components/KeyArea.svelte";
    import PreviewFinished from "$lib/components/preview/PreviewFinished.svelte";
</script>

<NavHome />

<div class="content">
    <!-- Top section text -->
    <div class="chapter">
        <h1>Hi there!</h1>
        <div class="chapter-intro">&#123; Who am I &#125;</div>
        <div class="highlight-text">
            I am an interface designer specializing in the visualization of data
            and information. I value research-driven projects that create
            meaningful results and grow out of user-centred processes fueled by
            curiosity, and fun teamwork. Here’s a peek into how I work and who I
            am as a designer.
        </div>
        <Button href="/about" type="internal">More about me :&#41;</Button>
    </div>

    <!-- Button section text -->
    <div class="chapter">
        <div class="chapter-intro">&#123; How to contact me &#125;</div>
        <div class="in-chapter">
            <Button href="mailto:vivien.serve@gmail.com" type="external">
                mail me: vivien.serve@gmail.com
            </Button>
            <Button
                href="https://www.linkedin.com/in/vivien-serve-25aa4a17a/?originalSubdomain=de"
                type="external"
            >
                or write a dm: LinkedIn
            </Button>
        </div>
    </div>

    <!-- Glipmse at work section -->
    <div class="chapter">
        <div class="chapter-intro">&#123; A glimpse at my work &#125;</div>
        <div class="in-chapter">
            <KeyArea variant="narratives" />
            <PreviewFinished href="/about" title="data visualization for the news" context="internship DIE ZEIT" year="2025" imageSrc="https://img.freepik.com/vektoren-kostenlos/einfaches-vibrierendes-katzenquadrat-meme_742173-4493.jpg?semt=ais_hybrid&w=740&q=80"/>
            <KeyArea variant="conceptual" />
            <PreviewFinished href="/about" title="ProLanes • Order to Cash" context="studies" year="2023/24" imageSrc="https://img.freepik.com/vektoren-kostenlos/einfaches-vibrierendes-katzenquadrat-meme_742173-4493.jpg?semt=ais_hybrid&w=740&q=80"/>
        </div>
    </div>
</div>

<style>
    .content {
        display: flex;
        flex-direction: column;
        gap: 38px;
    }

    .chapter {
        display: flex;
        flex-direction: column; /* vertical stacking */
        gap: 18px;
    }

    .in-chapter {
        display: flex;
        flex-direction: column;
        gap: 8px;
    }
</style>
