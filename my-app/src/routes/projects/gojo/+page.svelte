<script lang="ts">
    import ProjectHero from "$lib/components/projectBlocks/ProjectHero.svelte";
    import ImageAndText from "$lib/components/projectBlocks/ImageAndText.svelte";
    import TextAndText from "$lib/components/projectBlocks/TextAndText.svelte";
    import ImageAndImage from "$lib/components/projectBlocks/ImageAndImage.svelte";
</script>

<div class="project">
    <ProjectHero
        keyArea="narratives"
        title="Yeeees you found the hidden easter egg page"
        subtitle="because all of us anime fans love Satoru Gojo, and this is why"
        scope="Loving JJK (the anime), but mostly Gojo"
        tools="Stremio · Cinema · Wattpad Fanfiction (couldn't stop myself)"
        collaborators="Anna, I'm dragging you into this with me (not sorry)"
        context="I think we should all embrace our geekiness a little more."
        year="FOREVER"
        mediaType="image"
        mediaSrc="https://static0.gamerantimages.com/wordpress/wp-content/uploads/2023/08/collage-maker-08-aug-2023-01-02-pm-1287.jpg"
    />

    <ImageAndText
        imageSrc="https://www.belloflostsouls.net/wp-content/uploads/2024/03/gojo-students.jpg"
        quote="Satoru Gojo (五ご条じょう悟さとる Gojō Satoru) is one of the main [figures] of the Jujutsu Kaisen series. He is a special grade jujutsu sorcerer and widely recognized as the strongest in the world. "
        quoteSource="Jujutsu Kaisen Wiki"
        chapter="Who is satoru gojo"
        body="Gojo is the teacher of the protagonists of JJK. He is not the main character, but he is probably the most beloved (at least according to the sheer amount of fan fiction content about him). With his cursed techniques Limitless and Six Eye, he is the strongest sorcerer. This has an effect on his enormously arrogant personality, which we love, because deep down, Gojo is naturally good. He is goofy and warm-hearted, but also strong and rigorous towards his enemies (I swear this is a fangirl speaking)."
    />

    <ImageAndText
        imageSrc="https://i.redd.it/e3zaq33rfn791.jpg"
        quote="He's super cocky, but strong enough to actually back it up. Plus, his strength his more complicated than a lot of OP characters because of the complexity of his power [...]. And he's hot"
        quoteSource="DomHyrule on Reddit"
        chapter="Why do we love Gojo"
        body="His blue eyes! His character and the way he carries himself are incredibly attractive... but above all, his blue eyes. Seriously, he's a really interesting character with a heartbreaking backstory (really, if you have time, read or watch it, because it's so painful). Fortunately, I'm not the only person who's concerned with why Gojo is so likable."
        linkHref="https://www.youtube.com/watch?v=oU_OFak0csU"
        linkLabel="Why everybody loves gojo video"
    />

    <ImageAndImage 
    leftSrc="https://i1.sndcdn.com/artworks-vzvYkPmzB5nuo1oT-yg9zfw-t500x500.jpg"
    rightSrc="https://i.pinimg.com/736x/dc/67/f5/dc67f5587fa604c32fada9ccbe6d65d6.jpg"/>

    <ImageAndText
        imageSrc="https://uploads.jovemnerd.com.br/wp-content/uploads/2024/05/satoru_gojo_curiosidades__2h4a0242x.jpg"
        chapter="JJK and the female gaze"
        body="Gojo exemplifies an interesting (and, in my opinion, fantastic) phenomenon in JJK: the deliberate inclusion of content for the female gaze. This is even more impressive given that, as a shonen anime, it is typically aimed at young men. But women, as well as men in JJK, act in ways that are clearly fan service for women."
        linkHref="https://www.youtube.com/watch?v=vSpAIw7iEEM"
        linkLabel="Jujutsu Kaisen and the female gaze video"
        quote="In a world ordered by sexual imbalance, pleasure in looking has been split between active male and passive/female. The determining male gaze projects its phantasy on to the female figure which is styled accordingly. In their traditional exhibitionist role women are simultaneously looked at and displayed, with their appearance coded for strong visual and erotic impact."
        quoteSource="Mulvey, L., & Pleasure, V. (1975). Narrative cinema'. Screen, 16(3), 6-18."
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
