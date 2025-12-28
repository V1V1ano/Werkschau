<script lang="ts">
    import ProjectHero from "$lib/components/projectBlocks/ProjectHero.svelte";
    import ImageAndText from "$lib/components/projectBlocks/ImageAndText.svelte";
    import TextAndText from "$lib/components/projectBlocks/TextAndText.svelte";
    import ImageAndImage from "$lib/components/projectBlocks/ImageAndImage.svelte";
    import NextProjectTeaser from "$lib/components/projectBlocks/NextProjectTeaser.svelte";
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
        body={[
            "Imagine a world a few decades from now where smartphones are a relict of the past and technology has become deeply immersive. Digital elements merge with physical experiences, altering how reality is perceived and understood. We call these enhancements phygital layers. We call this environment a phygital one.",
            "This project explores how such technology reshapes communication and relationships. As individuals curate their own phygital layers, their realities become increasingly hyper-individual, which affects their perception and social interaction. Through a speculative narrative, the project highlights how beliefs and technological dependency emerge in personal, public and sensitive spaces. It asks questions about reality, responsibility, and communication.",
        ]}
        chapter="Project summary"
        linkHref="https://www.youtube.com/watch?v=FCa8ZMvG0qM"
        linkLabel="video documentation"
        caption="Spaces restrict and enable technology"
    />

    <TextAndText
        chapter="research"
        leftQuote="In an era marked by rapid technological advancements, democracies face unprecedented challenges that transcend political institutions and reach into the fabric of everyday life."
        leftQuoteSource="Altshuler et al. (2025). IPPSO–Transdisciplinary Research on Legal, Public Policy, and Design Perspectives for Immersive Phygital Public Spaces in Smart Cities."
        rightBody="To explore people’s emotional responses to phygital technology and the socio-economic structures that result from it, we employed future wheel techniques, system mapping, and other speculative storytelling methods. To address potential social conflicts, we experimented with multiple perspectives and characters, each with a different level of reliance on phygital software. We drew inspiration from current attitudes towards smartphones and social media. Rather than focusing on extremes, we believe the most interesting insights lie in the nuances."
    />

    <ImageAndImage
        leftSrc="https://wallpapers-clan.com/wp-content/uploads/2023/12/jujutsu-kaisen-grimacing-satoru-gojo-wallpaper-scaled.jpg"
        leftLabel="futures wheel"
        leftCaption="The Futures Wheel is an explorative method used to structure and visualize direct and indirect effects of changes."
        rightSrc="https://wallpapers.com/images/featured/gojo-satoru-pictures-8sz62hlsg1epni6l.jpg"
        rightCaption="Different stakeholders rely on omnipresent sensory-altering techniques in different ways."
    />

    <TextAndText 
    chapter="realisation"
    leftHighlight="Person-to-person relationships are shaped by hyper-individual realities arising from personal phygital layers and social norms embedded in the space. To demonstrate this ambiguity, the narrative unfolds across three spaces: the personal, the public and the sensitive."
    rightBody="We expressed our thought process in a video which uses parallel points of view. Even though our focus lies on person-to-person relationships, intra-personal, and person-to-space relationships overlap. A group of four old classmates, differenting greatly in their use and reliance on sensory altering technique, meet again. They start in the personal space of one person, moving through the street, which is an open space, and approach a senstive space, a cemetery. Conversations as well as their behaviour in these spaces demonstrates their fragmentation and conflict in finding common ground."
    />

     <ImageAndImage
        leftSrc="https://images.cgames.de/images/gsgp/290/jujutsu-kaisen-gojo-satoru_6307704.jpg"
        leftCaption="In a phygital world, spaces are affected by, and affect, sensory-altering techniques."
        rightSrc="https://static0.cbrimages.com/wordpress/wp-content/uploads/2023/05/jujutsu-kaisen-gojo-223.jpg?w=1200&h=628&fit=crop"
        rightCaption="One scene is experienced sharply differently among the individuals of the story."
    />

    <TextAndText 
    chapter="reflection"
    leftHighlight="I want to help people imagine and critically reflect futures."
    rightBody="This project aims to spark debate around the legal dimensions: What rights do we have as senders and recipients of information? Can intent ever be guaranteed in how a message is perceived? And can we define a moral compass today that accounts for diverse beliefs, ethics, and legal frameworks? Throwing questions into the future and pulling them back into the present proved to be one of the most interesting challenges for me as a designer."
    />

    <NextProjectTeaser
        href="/about"
        src="https://i.pinimg.com/736x/d0/82/31/d082311ac3b94b11708e0dc82793bc84.jpg"
        tag="test"
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
