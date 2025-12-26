<script>
  import NavAbout from "$lib/components/nav/NavAbout.svelte";
  import PreviewFinished from "$lib/components/preview/PreviewFinished.svelte";
  import Button from "$lib/components/Buttons/Button.svelte";
  import KeyArea from "$lib/components/KeyArea.svelte";
</script>

<NavAbout />

<div class="content">
  <!-- Top section text -->
  <div class="intro-grid">
    <div class="intro-image">
      <img
        src="https://blogs.urz.uni-halle.de/memekultur/files/elementor/thumbs/Meme2-oxj1km9nq1ecvybvcqox9hi8q6sbj6pnh6r4ugwq00.jpg"
        alt="Portrait of Vivien Serve"
      />
    </div>

    <div class="chapter">
      <div class="chapter-intro">&#123; Who am I &#125;</div>
      <div class="highlight-text">
        I am an interface designer specializing in the visualization of data and
        information. I value research-driven projects that create meaningful
        results and grow out of user-centred processes fueled by curiosity, and
        fun teamwork. Here’s a peek into how I work and who I am as a designer.
      </div>
    </div>
  </div>

  <!-- Information about what and who -->
  <div class="chapter">
    <div class="chapter-intro">&#123; Skills &#125;</div>
    <div class="in-chapter">
      UI / UX Design · Figma and Adobe CC <br /> Service Design · User–centric
      ideation <br />
      Front–end development · SvelteKit
    </div>
  </div>

  <div class="chapter">
    <div class="chapter-intro">&#123; Milestones &#125;</div>
    <div class="in-chapter">MUSS NOCH GEMACHT WERDEN</div>
  </div>

  <div class="chapter">
    <div class="chapter-intro">&#123; People I xx working with &#125;</div>
    <div class="in-chapter">
      Jacky Grob <br />
      Jost Götte <br />
      Mauzen Crew <br />
    </div>
  </div>

  <!-- Projects I'm working on -->
  <div class="chapter">
    <div class="chapter-intro">&#123; A glimpse at my work &#125;</div>
    <!-- Project grid is used to align content in a grid on desktop -->
    <div class="project-grid">
      <div class="in-chapter">
        <KeyArea variant="narratives" />
        <PreviewFinished
          href="/about"
          title="Data visualization for the news"
          context="Internship DIE ZEIT"
          year="2025"
          mediaType="video"
          posterSrc="https://img.freepik.com/vektoren-kostenlos/einfaches-vibrierendes-katzenquadrat-meme_742173-4493.jpg?semt=ais_hybrid&w=740&q=80"
          videoSrcWebm="/project-images/ZEIT/proteine.webm"
        />
      </div>
      <div class="in-chapter">
        <KeyArea variant="conceptual" />
        <PreviewFinished
          href="/about"
          title="ProLanes • Order to Cash"
          context="Studies"
          year="2023/24"
          mediaType="image"
          mediaSrc="/project-images/ProLanes/Teaser.png"
        />
      </div>
    </div>
  </div>
</div>

<style>
  .content {
    display: flex;
    flex-direction: column;
    gap: 48px;
    margin: 48px 0px;
  }

  /* This needs to mimic content */
  .intro-grid {
    display: flex;
    flex-direction: column;
    gap: 48px;
  }

  .chapter {
    display: flex;
    flex-direction: column; /* vertical stacking */
    gap: 18px;
  }

  .intro-image {
    display: flex;
    justify-content: flex-end; /* right aligned */
  }

  .intro-image img {
    width: 185px;
    height: 185px;
    object-fit: cover;
  }

  /* this needs to mimic chapter */
  .project-grid {
    display: flex;
    flex-direction: column;
    gap: 18px;
  }

  .in-chapter {
    display: flex;
    flex-direction: column;
    gap: 8px;
  }

  @media (min-width: 900px) {
    .project-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      align-items: start;
      gap: 36px;
    }

    .chapter {
      gap: 24px;
    }

    .intro-image img {
      width: 260px;
      height: 260px;
    }

    .in-chapter {
      gap: 18px;
    }

    .intro-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 48px;
      padding: 48px 0;
    }

    .content {
      gap: 96px;
      margin-bottom: 96px;
    }
  }
</style>
