<script>
  import NavAbout from "$lib/components/nav/NavAbout.svelte";
  import PreviewUnfinished from "$lib/components/preview/PreviewUnfinished.svelte";
  import KeyArea from "$lib/components/KeyArea.svelte";
  import CardCV from "$lib/components/cards/CardCV.svelte";
  import MilestoneShuffle from "$lib/components/MilestoneShuffle.svelte";
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
    <div class="in-chapter">
      <MilestoneShuffle
        headline="Bachelor in Potsdam, at FH;P (hopefully)"
        buttonLabel="Click to Shuffle how this affected me"
        items={[
          "Didn’t like pizza before. Now, I like it (most of the times I guess)",
          "Learned to trust iteration over the ‘perfect idea’.",
          "Discovered: writing is also interface design.",
          "Got better at saying no to shiny features (sometimes).",
        ]}
      />
    </div>
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
        <KeyArea variant="speculative" />
        <PreviewUnfinished
          title="Navigating futures with data visualization → interpretation-visualization as speculative medium to navigate future phenomena"
          context="Bachelor thesis"
          mediaType="image"
          mediaSrc="https://i1.sndcdn.com/artworks-WwWAK5ilqjIKiGyS-YBzzgA-t500x500.jpg"
        />
      </div>
      <div class="in-chapter">
        <KeyArea variant="ui" />
        <PreviewUnfinished
          title="MichAIL – music recommendation meets explainable AI"
          context="Personal project w/ Jacky & Jost"
          mediaType="image"
          mediaSrc="https://i1.sndcdn.com/artworks-WwWAK5ilqjIKiGyS-YBzzgA-t500x500.jpg"
        />
      </div>
    </div>
  </div>

  <!-- Relevant work experience -->
  <div class="chapter">
    <div class="chapter-intro">&#123; selected Work experience &#125;</div>
    <div class="in-chapter">
      <CardCV
        from="2025"
        to="NOW"
        title="Data visualization designer"
        place="@ DIE ZEIT"
        logoSrc="/logos/Zeit.png"
        linkHref="https://www.zeit.de/autoren/S/Vivien_Serve/index"
        linkLabel="Author Profile"
        linkType="external"
      />
      <CardCV
        from="2023"
        to="NOW"
        title="Data visualization designer"
        place="@ Datawrapper"
        logoSrc="/logos/Datawrapper.png"
        linkHref="https://www.datawrapper.de/blog/say-hi-to-vivien"
        linkLabel="Blog Article"
        linkType="external"
      />
      <CardCV
        from="2021"
        to="2023"
        title="Service Designer and Front-end"
        place="@ Helmholtz Metadata Collaboration"
        logoSrc="/logos/hmc.png"
        linkHref="https://datascience.codata.org/articles/10.5334/dsj-2024-041"
        linkLabel="Paper"
        linkType="external"
      />
    </div>
  </div>

  <!-- Education -->
  <div class="chapter">
    <div class="chapter-intro">&#123; education &#125;</div>
    <div class="in-chapter">
      <CardCV
        from="2021"
        to="NOW"
        title="Interface Design"
        place="@ University of Applied Sciences Potsdam"
        logoSrc="/logos/FHP.png"
      />
      <CardCV
        from="2021"
        to="NOW"
        title="Interaction Design"
        place="@ National Taipei University of Technology"
        logoSrc="/logos/taipei.png"
      />
    </div>
  </div>

  <!-- Education -->
  <div class="chapter">
    <div class="chapter-intro">&#123; education &#125;</div>
    <div class="in-chapter">
      <CardCV
        from="2021"
        to="NOW"
        title="Mauzen Festival"
        place="w/ Garzelice e.V. (Founding member & deputy cash auditor)"
        logoSrc="/logos/mauzen.png"
        linkHref="https://mauzen-festival.de/"
        linkLabel="Website"
        linkType="external"
      />
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
      grid-template-columns: minmax(0, 1fr) auto;
      grid-template-areas: "text image";
    }

    .intro-grid > .chapter {
      grid-area: text;
      max-width: 47vw;
    }

    .intro-grid > .intro-image {
      grid-area: image;
      justify-self: end;
    }

    .content {
      gap: 96px;
      margin-bottom: 96px;
    }
  }
</style>
