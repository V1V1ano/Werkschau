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
    collaborators={["Leonidas von Bothmer", "Natalia Pawlik", "IPPSO @ UCLAB"]}
    context={["University", "w/ Prof. Boris Müller", "Markus Kreutzer"]}
    year="2024/25"
    linkHref="https://uclab.fh-potsdam.de/ippso/"
    linkLabel="IPPSO Project"
    mediaType="image"
    mediaSrc="/project-images/Phygital/teaser.png"
/>

<ImageAndText
  imageSrc="https://i.pinimg.com/originals/2e/bb/01/2ebb017eb0feb6824440d3135713b002.jpg"
  text="Some text…"
  chapter="Project summary"
  caption="This is a figcaption that helps people…"
  credit="©ALEXANDER MOLKENTHIN"
/>

<ImageAndText
  imageSrc="https://wallpapers-clan.com/wp-content/uploads/2023/12/jujutsu-kaisen-grimacing-satoru-gojo-wallpaper-scaled.jpg"
  text="test"
  chapter="test"
  label="EXPLORATORY VIEW"
/>

<ImageAndText
  imageSrc="https://wallpapers.com/images/featured/gojo-satoru-pictures-8sz62hlsg1epni6l.jpg"
  chapter="test"
  text="No meta here, just image + text."
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