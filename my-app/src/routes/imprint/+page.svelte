<script>
  import NavAbout from "$lib/components/nav/NavAbout.svelte";
</script>

<NavAbout />

<div class="content">
  <h1>Imprint</h1>

  <p class="block">
    <span class="table-label">Information in accordance with § 5 TMG</span><br />
    <span class="table-value">
      Vivien Serve<br />
      Benzstraße 13<br />
      14482 Potsdam<br />
      Germany
    </span>
  </p>

  <p class="block">
    <span class="table-label">Contact</span><br />
    <span class="table-value">
      Phone: +49 1516 8175398<br />
      Email: vivien.serve@gmail.com 
    </span>
  </p>

  <p class="block">
    <span class="table-label">
      Responsible for content
    </span><br />
    <span class="table-value">
      Vivien Serve<br />
      Benzstraße 13<br />
      14482 Potsdam
    </span>
  </p>

   <p class="block">
    <span class="table-label">
      Design and Production
    </span><br />
    <span class="table-value">
      Vivien Serve
    </span>
  </p>

  <p class="block">
    <span class="sub-headline">Liability for Content</span> <br/><br/>
    <span class="body">
      As a service provider, I am responsible for my own content on these pages
      in accordance with Section 7 (1) TMG and general laws. According to Sections
      8 to 10 TMG, however, I am not obligated to monitor transmitted or stored
      third-party information or to investigate circumstances that indicate
      illegal activity.
    </span>
  </p>

  <p class="block">
    <span class="sub-headline">Liability for Links</span><br/><br/>
    <span class="body">
      This website may contain links to external third-party websites over whose
      content I have no control. Therefore, I cannot assume any liability for
      such external content. The respective provider or operator of the linked
      pages is always responsible for their content.
    </span>
  </p>

  <p class="block">
    <span class="sub-headline">Copyright</span><br/><br/>
    <span class="body">
      The content and works created by the site operator on these pages are
      subject to German copyright law. Third-party contributions are identified
      as such. Any reproduction, editing, distribution, or any form of
      exploitation beyond the limits of copyright law requires the written
      consent of the respective author.
    </span>
  </p>

  <p class="block">
    <span class="sub-headline">Fonts</span><br/><br/>
    <span class="body">
      Special thanks to <strong>ABC Dinamo</strong> for providing the fonts used
      on this website: ABC Gaisyr, ABC Monument Grotesk, and ABC Diatype.
    </span>
  </p>
</div>

<style>
  .content {
    display: flex;
    flex-direction: column;
    margin: 48px 0px;
  }
</style>
