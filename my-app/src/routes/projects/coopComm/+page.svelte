<script lang="ts">
    import ProjectHero from "$lib/components/projectBlocks/ProjectHero.svelte";
    import ImageAndText from "$lib/components/projectBlocks/ImageAndText.svelte";
    import TextAndText from "$lib/components/projectBlocks/TextAndText.svelte";
    import ImageAndImage from "$lib/components/projectBlocks/ImageAndImage.svelte";
    import NextProjectTeaser from "$lib/components/projectBlocks/NextProjectTeaser.svelte";
</script>

<div class="project">
    <ProjectHero
        keyArea="conceptual"
        title="Co-op.Comm"
        subtitle="Creating scalable semantic organigrams for co-operatives"
        scope="Research · Concept · Design"
        tools="Figma"
        collaborators="10 co-operatives / collectives in Berlin / Potsdam"
        context={[
            "University",
            "w/ Prof. Dr. Marian Dörk",
            "Prof. Myriel Milicevic",
        ]}
        year="2023"
        linkHref="https://infovis.fh-potsdam.de/organigrams/"
        linkLabel="Result website"
        mediaType="image"
        mediaSrc="/project-images/CoopComm/teaser.gif"
    />

    <ImageAndText
        imageSrc="/project-images/CoopComm/poster.jpeg"
        body={[
            "Ten cooperatives from Potsdam and Berlin opened their doors to share how they organize working together. Beyond formal legal structures, cooperatives reveal their strength in situational responses to economic and social challenges – shaped by open and diverse communication cultures.",
            "Co-op.comm makes these communication structures visible. It encodes communicational structures, rooms for communication, topic, members, and problems. It showcases the uniqueness of each organiation, questioning whether communication itself can function as an organizational chart. ",
        ]}
        chapter="Project summary"
        linkHref="https://fhp.incom.org/project/25346/open-to-public"
        linkLabel="full written documentation"
        caption="The exhibition poster showcases building blocks & examples"
        credit="©Alexander Molkenthin"
    />

    <TextAndText
        chapter="RESEARCH & Realisation"
        leftHighlight="Members of co-operatives communicate with each other in interwoven, self-determined and fluid ways. Through this unique mode of communication, they jointly develop sustainable and subjective solutions."
        rightBody={[
            "The focus on communication emerged during discussions with individuals living and working in cooperative environments, where decisions were frequently described as processes that would be 'talked through'. Communication can be understood as a reflection of the cooperative structure itself. My design aims to highlight what distinguishes cooperative communication from the one in other work settings. It emphasises its intimacy through shared ownership and responsibility, and demonstrates that no cooperative functions in the same way as another.",
            "Research revealed that cooperative communication is inherently multi-layered, spanning personal, work-related and cooperative-specific exchanges which often overlap across entities. These communicative layers are encoded as distinct visual variables within the visualization. Together, they form an organigrammatic structure that builds up subsequently.",
        ]}
    />
     <ImageAndImage
        leftSrc="/project-images/CoopComm/Layer_of_communication.png"
        leftCaption="Layers of communication in a co-operative from base to surface"
        rightSrc="/project-images/CoopComm/coop.webm"
        rightCaption="each visual variable corresponds to one layer of communication"
    />

   
    <TextAndText
        chapter="final product"
       leftQuote="The shift from exploration to narration puts ephemeral aspects of interactive visualizations up for debate and reflection, encouraging viewers to critically engage with data visualization. Conversely, shifting from narration to exploration challenges the authority of a singular story, enabling viewers to question predefined interpretations and construct their own pathways through the data."
       leftQuoteSource="Morini et al. (2025). Critical Interactivity: Exploration and Narration in Data Visualization."
       rightBody="The application offers two modes: explorative (dialogue view) and narrative (monologue view). These modes allow newcomers to learn the visual language and enable experienced users to navigate by tapping and filtering. Visual variables are enriched with tooltips that offer insight into communication spaces, challenges, and key topics.  It is realised as a website prototype encoding a preliminary set of co-operatives and collectives."
       rightLinkLabel="Prototype"
       rightLinkHref="https://www.figma.com/proto/d8CQHPhjl30T0BQ1ud5Z40/Unfolding-the-edges-of-communication?page-id=579%3A439053&node-id=588-445426&viewport=2015%2C-1270%2C0.66&t=S9UsaJn8HLkmGTQz-1&scaling=contain&content-scaling=fixed&starting-point-node-id=588%3A445426&show-proto-sidebar=1"
    />

     <ImageAndImage
        leftSrc="/project-images/CoopComm/Monologue_View.png"
        leftLabel="monologue view"
        rightSrc="/project-images/CoopComm/Dialogue_View.png"
        rightLabel="Dialogue view"
    />
   

    <TextAndText
        chapter="reflection"
        leftHighlight="I want to portray meaningful qualitative data through novel concepts."
        rightBody="This project taught me that data visualization can be extremely valuable to the people it depicts. When their own experiences and stories are incorporated, it can help them reflect on and understand themselves. This project showcases my favorite mode of working: collecting data through meaningful encounters, taking a user-centric approach, and transcending classical forms of visualization."
    />

    <NextProjectTeaser
        href="/projects/phygital"
        src="/project-images/Phygital/teaser.png"
        tag="Fragmented Realities"
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
