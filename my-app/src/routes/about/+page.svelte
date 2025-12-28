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
        src="/profile.jpg"
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
  <div class="column-on-desktop">
    <div class="chapter">
      <div class="chapter-intro">&#123; Skills &#125;</div>
      <div class="in-chapter">
        UI / UX Design · Figma and Adobe CC <br /> Service Design · User–centric
        ideation <br />
        Front–end development · SvelteKit
      </div>
    </div>

    <div class="chapter chapter--narrow">
      <div class="chapter-intro">&#123; People I &lt;3 working with &#125;</div>
      <div class="in-chapter">
        Jacky Grob <br />
        Jost Götte <br />
        Mauzen Crew <br />
      </div>
    </div>

    <div class="chapter">
      <div class="chapter-intro">&#123; Milestones &#125;</div>
      <div class="in-chapter">
        <MilestoneShuffle
          headline="Bachelor in Potsdam, at FH;P (hopefully)"
          buttonLabel="Click to Shuffle my Discoveries"
          items={[
            "Design is an attitude that I must regularly evaluate, adapt, verify, and falsify.",
            "Design and my own personality are intertwined; convictions are brought into the equation; and discarded. My designs reflect my convictions and interests while maintaining professional distance.",
            "Design is both a collaborative process and a competitive arena. My only option is to treat it as an opportunity for growth.",
            "Friendships are never static; they are always in a state of flux and must not be taken for granted. However, with effort and time, it is possible to maintain them across continental borders.",
            "If you're in Potsdam, you should try a fish sandwich from the vendor at Nauener Tor market. It's better than in Hamburg! (Apart from Fabio's Fischhütte.) ",
            "Design is an eternal negotiation between inspiration and creation. The concept of authorship is a difficult one, but one that is worth discussing.",
            "I now think that pizza isn't such bad food after all, at least most of the time. Especially when you're sitting at PiPaSa at 3am.",
            "I have learned to stand up for my position as a woman in interface design, to recognize our underrepresentation and to oppose it. And to be able to see this disadvantage but also see other privileges that I have.",
            "The third semester was the best, when I was in the student council, when we came up with a new event every week, when I met so many of my friends, and when I briefly thought that the university belonged to us.",
            "In Taiwan, I learnt that the best dumplings are usually found in the most unappealing restaurants; queuing for the MRT is much quicker than everyone rushing in at once (why Germany?); and that life is good if you hike up a mountain once a week.",
            "The sound in the Columbia Hall isn't that bad after all cc Jacky.",
            "I appreciate the geeky and childish sides of people the most. Embracing my own has brought me closer to myself and to many of my friends."
          ]}
        />
      </div>
    </div>
  </div>

  <!-- Projects I'm working on -->
  <div class="chapter">
    <div class="chapter-intro">&#123; What I'm currently working on &#125;</div>
    <!-- Project grid is used to align content in a grid on desktop -->
    <div class="project-grid">
      <div class="in-chapter">
        <KeyArea variant="speculative" />
        <PreviewUnfinished
          title="Navigating futures with data visualization → interpretation-visualization as speculative medium to navigate future phenomena"
          context="Bachelor thesis"
          mediaType="image"
          mediaSrc="/project-images/Unfinished/bachelorthesis.png"
        />
      </div>
      <div class="in-chapter">
        <KeyArea variant="ui" />
        <PreviewUnfinished
          title="MichAIL – music recommendation meets explainable AI"
          context="Personal project w/ Jacky & Jost"
          mediaType="image"
          mediaSrc="/project-images/Unfinished/michail.png"
        />
      </div>
    </div>
  </div>

  <div class="column-on-desktop">
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

    <!-- Fun -->
    <div class="chapter">
      <div class="chapter-intro">&#123; fun &#125;</div>
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
</div>

<style>
  .content {
    display: flex;
    flex-direction: column;
    gap: 48px;
    margin: 48px 0px;
  }

  /* needs to mimic content, because just used for column layout on mobile */
  .column-on-desktop {
    display: flex;
    flex-direction: column;
    gap: 48px;
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
      padding-bottom: 192px;
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

    .column-on-desktop {
      display: flex;
      flex-direction: row;
      width: 100%;
      gap: 36px;
      align-items: start;
    }

    /* default columns */
    .column-on-desktop > .chapter {
      flex: 1 1 0;
      min-width: 0;
    }

    /* 👇 make only the people column smaller */
    .column-on-desktop > .chapter--narrow {
      flex: 0.7 1 0; /* tweak this value */
    }
  }
</style>
