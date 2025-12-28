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
        title="ProLanes • Order to Cash"
        subtitle="Speculative redesign of ERP software for SAP"
        scope="Research · Concept · Design ·  Prototyping "
        tools="Figma · SAP BPMN"
        collaborators={["Jonathan Dahle", "SAP"]}
        context={["University", "w/ Prof. Boris Müller"]}
        year="2023/24"
        linkHref="https://youtu.be/IIxamx7BFFk?si=QNLKro95nIgB4UDJ"
        linkLabel="Video Documentation"
        mediaType="image"
        mediaSrc="/project-images/ProLanes/Teaser.png"
    />

    <ImageAndText
        imageSrc="https://i.pinimg.com/originals/2e/bb/01/2ebb017eb0feb6824440d3135713b002.jpg"
        body="ProLanes emerged from a cooperation with SAP that challenged established ways of visualizing end-to-end business processes, using Order-to-Cash as a case study. Rather than redesigning existing ERP (Enterprise Resource Planning) software, the project critically examines how complex processes are represented and understood. We explore new visual and interactive formats grounded in data visualization principles. This resulted in a speculative yet operational prototype that translates abstract process logic into a spatial, task-oriented interface: ProLanes."
        chapter="Project summary"
        linkHref="https://fhp.incom.org/project/27196/open-to-public"
        linkLabel="written documentation"
        caption="Presenting ProLanes in the sap Innovation centre"
    />

    <ImageAndText
        imageSrc="https://wallpapers-clan.com/wp-content/uploads/2023/12/jujutsu-kaisen-grimacing-satoru-gojo-wallpaper-scaled.jpg"
        body="The visual concept of ProLanes draws inspiration from train route visualizations, where lines, stations, and intersections convey information about progression, dependencies, and direction. Processes are mapped as routes, each task is represented by a station. Orders move through the system like trains passing stations (=tasks), making flow and responsibility legible at a glance. Importantly, the visualization is contextualized: each person working with an order sees a different section of the network tailored to their responsibilities interfaces with others, either co-workers or customers. This role-specific perspective helps workers locate orders within the overall process without being overwhelmed by irrelevant details."
        chapter="The visual analogy"
        caption="The Process Order to Cash looks different depending on the employees needs"
        highlight="The visual analogy of train routes helps employees follow complex processes by enabling them to focus on their own tasks and responsibilities, as well as their intersections with other stakeholders."
    />

    <ImageAndText
        imageSrc="https://wallpapers.com/images/featured/gojo-satoru-pictures-8sz62hlsg1epni6l.jpg"
        quote="[A]n InfoVis tool that exhibits [fluid interactivity] in all aspects will transform the sensemaking process into an efficient, illuminating, and even enjoyable experience because it helps the user stay in the flow of the work process."
        quoteSource="Elmqvist et al. (2011). Fluid interaction for information visualization."
        body="ProLanes is not limited to monitoring: users can process orders directly within the visualization. Each process step is an actionable tickets. The coupling of overview and action supports responsibility, faster problem resolution, and smoother cross-department collaboration. Management perspectives additionally enable live monitoring of KPIs and bottlenecks across the process. As speculative software, ProLanes demonstrates how alternative visual logics can reshape everyday work in complex systems."
        chapter="operationalisation"
        caption="Direct task processing in ProLanes"
        linkHref="https://youtu.be/G62mNC2b5bw?si=zGvlhK_qRDew1Wim"
        linkLabel="TEDx Talk by Prof. Boris Müller"
    />

    <TextAndText
        chapter="reflection"
        leftHighlight="I want to create visualizations that are more than a picture – but a useful tool that improves peoples lives."
        rightBody="ProLanes shows how visualisation can simplify complex processes. I see particular potential in visualisation that is not rigid, but rather context-dependent and directly operationalisable. I can potentially function as a real UI modular system. The creation of speculative software such as ProLanes demonstrates the value of such as a source of inspiration. This is particularly valuable in the context of long-established systems, such as SAP's ERP systems. "
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
