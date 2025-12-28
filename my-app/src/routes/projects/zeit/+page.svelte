<script lang="ts">
    import ProjectHero from "$lib/components/projectBlocks/ProjectHero.svelte";
    import ImageAndText from "$lib/components/projectBlocks/ImageAndText.svelte";
    import TextAndText from "$lib/components/projectBlocks/TextAndText.svelte";
    import ImageAndImage from "$lib/components/projectBlocks/ImageAndImage.svelte";
    import NextProjectTeaser from "$lib/components/projectBlocks/NextProjectTeaser.svelte";
</script>

<div class="project">
    <ProjectHero
        keyArea="narratives"
        title="Internship • DIE ZEIT "
        subtitle="visualization for daily news"
        scope="Research & Data Collection · Data Wrangling · UI & UX Design · Creation of Visual Assets"
        tools="Figma · Svelte · QGIS · Datawrapper"
        collaborators="DIE ZEIT"
        context="internship"
        year="2025"
        mediaType="video"
        videoSrcWebm="/project-images/ZEIT/proteine.webm"
        linkLabel="My author profile"
        linkHref="https://www.zeit.de/autoren/S/Vivien_Serve/index"
    />

    <ImageAndText
        imageSrc="/project-images/ZEIT/teaser_quadrat.gif"
        body="During a six-month internship at ZEIT, my work focused on the intersection of journalism, design, and technology within the Data and Visualization Department. The core task was the design of interactive data articles that translated complex topics into accessible, mobile-first storytelling formats. Alongside developing interaction patterns and UI components beyond the existing corporate identity, the work included teaser visuals, editorial charts, interactive metrics, and graphic reviews. "
        chapter="summary"
        caption="A selection of feature images used for articles"
    />

    <TextAndText
        chapter="interaction patterns"
        leftBody="As a designer, I created new interaction patterns for exploring large data sets or adapted existing ones. While doing so, we experimented with a wide variety of interaction patterns, always adhering to the minimalist ZEIT design of UI components. One particularly interesting aspect was considering ways to help viewers navigate data sets, find themselves in them, and compare themselves with others."
    />

    <ImageAndImage
        leftSrc="/project-images/ZEIT/ruecktritte.webm"
        leftLabel="swipe interaction"
        rightSrc="/project-images/ZEIT/abitur.webm"
        rightLabel="Quiz Mode"
    />

    <ImageAndText
        chapter="responsive illustrations"
        caption="A selection of responsive illustrations used in articles"
        imageSrc="/project-images/ZEIT/responsiveIllustrationen.gif"
        quote="Mobile traffic market share is the largest in November 2025 with 67.5% of all Mobile traffic"
        quoteSource="similar web. (2025). Mobile vs. Desktop vs. Tablet Traffic Market Share"
        body="Articles in ZEIT regularly feature explanatory illustrations. Since their target audience accesses these articles on a wide variety of devices, illustrations must be prepared for every use case. Therefore, I created infographic elements in dark mode, light mode, for mobile and desktop. And that's for a wide variety of topics: from mitochondrial replacement therapy to attacks on Iran."
    />

    <ImageAndText
        chapter="mobile-friendly data storytelling"
        label="Project excerpt"
        imageSrc="/project-images/ZEIT/ZEIT-flow.png"
        body="Just as with illustrations, ZEIT articles focus on mobile-friendly data storytelling. This is particularly challenging when complex content and diverse interaction options should be conveyed. In this context, mobile first means not only reducing content to smaller screens, but also aligning narrative structures, interactions, and visual hierarchies from the beginning with shorter attention spans, vertical scrolling, and mobile intuitive usage. "
    />

    <TextAndText
        chapter="reflection"
        leftHighlight="I want to communicate topics in an accessible way, beyond the power users."
        rightBody="This internship offered me a wide range of learnings. Close collaboration with journalists and data specialists emphasized the importance of sensitivity, clarity, and responsibility when designing for a broad and diverse readership. Designing mobile-first data visualizations was both challenging and highly valuable, given that mobile devices are the primary way most readers engage with journalistic content. Working across a wide variety of topics and tools further deepened my understanding of how adaptable visual storytelling needs to be in a newsroom context – and beyond. "
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
