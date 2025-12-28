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
        title="The City as a Reading Rooms"
        subtitle="Collaborative exhibition about reading rooms in Potsdam"
        scope="Data collection & presentation"
        tools="Photogrammetry · Cutter · InDesign"
        collaborators="Université de Strasbourg"
        context={["University", "w/ Prof. Christina Poth", "Felix Walser"]}
        year="2025"
        linkHref="https://dujour.uber.space/thecityasareadingroom/"
        linkLabel="Reading Rooms"
        mediaType="image"
        mediaSrc="/project-images/ReadingRooms/big_picture.png"
    />

    <ImageAndText
        imageSrc="/project-images/ReadingRooms/glue-on-the-floor.jpg"
        body="This exhibition emerged from a collaboration with the Université de Strasbourg, during which reading spaces in Potsdam and Strasbourg were explored, documented, and discussed. The project critically reflects on the act of reading and the conditions that shape reading spaces, inviting visitors to immerse themselves in these environments and conversations. Participation is encouraged through a large floor map where visitors can add their own reading routes and locations, alongside a modular reading room designed for lingering. "
        chapter="project summary"
        caption="Visitors could mark their favourite reading room on the large map of Potsdam on the floor."
        credit="©Alexander Molkenthin"
    />

     <ImageAndText
        imageSrc="/project-images/ReadingRooms/3dScan.png"
       body="We collected and cartographed reading rooms in Potsdam, experiencing their offerings and atmospheres firsthand. To preserve these spaces, we created 3D scans that were later exhibited. We also spent time sitting in the reading rooms and writing short texts, capturing lived, sparked, or imagined experiences from the perspectives of visitors or even the books themselves. These texts resulted in riso-printed bookmarks that visitors could take home from the exhibition."
        chapter="research"
        caption="3D Scan of one Reading Room"
        credit="©Maurice Braatz & Me"
    />

    <TextAndText 
        leftHighlight="Everything can be a reading room. Everyone experiences reading differently: some seek solitude with a text, others connection through conversation, and some the desire to preserve what has been read."
        chapter="realisation"
        rightBody="The mapped reading spaces were made tangible in multiple ways. Participation was a central concern, which led to the creation of a large floor map of Potsdam where the documented reading spaces were located. Visitors were invited to place themselves and their own reading spaces onto the map. As a central element of the exhibition, the map was accompanied by images of the reading spaces and 3D scans. A particular highlight was a small reading room installed within the exhibition, where visitors could linger, exchange thoughts, read, and both retrace our experiences and add their own."
    />

    <ImageAndImage 
    leftSrc="/project-images/ReadingRooms/reading-room.jpeg"
    leftLabel="Reading room"
    leftCredit="©ALEXANDER MOLKENTHIN"
    rightSrc="/project-images/ReadingRooms/instructions-reading-room.jpg"
    rightLabel="map instructions"
    rightCredit="©ALEXANDER MOLKENTHIN"
    />

     <TextAndText 
        leftHighlight="I want to make data available through a plethora of mediums and tools."
        chapter="reflection"
        rightBody="Even though most of my work is situated in interface design, this project made clear a desire to move beyond the screen. It sparked an interest in designing more accessible experiences and working within participatory contexts. Visualization is not limited to digital interfaces; it can take on many different forms and exist across a wide range of spaces and interactions. "
    />

    <NextProjectTeaser
        href="/projects/zeit"
        src="/project-images/ZEIT/ZEIT-flow.png"
        tag="DIE ZEIT"
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
