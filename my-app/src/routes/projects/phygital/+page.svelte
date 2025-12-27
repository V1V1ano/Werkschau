<script lang="ts">
    import ProjectHero from "$lib/components/projectBlocks/ProjectHero.svelte";
    import ImageAndText from "$lib/components/projectBlocks/ImageAndText.svelte";
</script>

<div class="project">
    <ProjectHero
        keyArea="speculative"
        title="Phygital Layers to Fragmented Realities"
        subtitle="Speculative culturality rooted in immersive phygital technologies"
        scope="Research · Concept · Storytelling · Design ·  Video production"
        tools="Figma · various AI tool"
        collaborators={[
            "Leonidas von Bothmer",
            "Natalia Pawlik",
            "IPPSO @ UCLAB",
        ]}
        context={["University", "w/ Prof. Boris Müller", "Markus Kreutzer"]}
        year="2024/25"
        linkHref="https://uclab.fh-potsdam.de/ippso/"
        linkLabel="IPPSO Project"
        mediaType="image"
        mediaSrc="/project-images/Phygital/teaser.png"
    />

    <ImageAndText
        imageSrc="https://i.pinimg.com/originals/2e/bb/01/2ebb017eb0feb6824440d3135713b002.jpg"
        body="Imagine a world a few decades from now where smartphones are a relict of the past and technology has become deeply immersive. Digital elements merge with physical experiences, altering how reality is perceived and understood. We call these enhancements phygital layers. We call this environment a phygital one.
        This project explores how such technology reshapes communication and relationships. As individuals curate their own phygital layers, their realities become increasingly hyper-individual, which affects their perception and social interaction. Through a speculative narrative, the project highlights how beliefs and technological dependency emerge in personal, public and sensitive spaces. It asks questions about reality, responsibility, and communication."
        chapter="Project summary"
        caption="Spaces restrict and enable technology"
    />

    <ImageAndText
        imageSrc="https://wallpapers-clan.com/wp-content/uploads/2023/12/jujutsu-kaisen-grimacing-satoru-gojo-wallpaper-scaled.jpg"
        body="test"
        chapter="test"
        label="EXPLORATORY VIEW"
        highlight="Person-to-person relationships are shaped by hyper-individual realities arising from personal phygital layers and social norms embedded in the space. To demonstrate this ambiguity, the narrative unfolds across three spaces: the personal, the public and the sensitive."
        linkLabel="more information here"
        linkHref="https://example.com"
    />

    <ImageAndText
        imageSrc="https://wallpapers.com/images/featured/gojo-satoru-pictures-8sz62hlsg1epni6l.jpg"
        chapter="test"
        body="No meta here, just image + text."
        quote="CO–OP.COMM explores whether communication patterns can function as organisational charts…"
        quoteSource="bla bla bla john bla bla"
    />
</div>

<style>
    .project {
        display: flex;
        flex-direction: column;
        gap: 38px;
    }

    @media (min-width: 900px) {
        .project {
            gap: 64px;
        }
    }
</style>
