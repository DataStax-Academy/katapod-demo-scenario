<!-- TOP -->
<div class="top">
  <img class="scenario-academy-logo" src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-2023.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">Katapod Quickstart</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:academy@datastax.com">email</a>.</span>
  </div>
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
  <a title="Back" href='command:katapod.loadPage?[{"step":"step5"}]' class="btn btn-dark navigation-top-left">
    ⬅️ Back
  </a>
  <span class="step-count">Step 6</span>
  <a title="Next (Astra DB)" href='command:katapod.loadPage?[{"step":"step7-astra"}]' 
    class="btn btn-dark navigation-top-right"
    style="margin-left: 8px;"
  >
    Next (Astra DB) ➡️
  </a>
  <a title="Next (Cassandra)" href='command:katapod.loadPage?[{"step":"step7-cassandra"}]' class="btn btn-dark navigation-top-right">
    Next (Cassandra) ➡️
  </a>
</div>

<!-- CONTENT -->
<div class="step-title">Navigation and custom HTML</div>

The markdown step files contain quite some HTML: at the moment, for example,
header and navigation buttons are all written explicitly in the markdown files
as raw HTML (also the `<details>` blocks are possible because of this).

Nothing prevents you from further mixing markdown and custom HTML, for example
if you want to alter the appearance of the navigation.

<div style="border-width: 1px; border-color: magenta; background-color: gold;">
  <p style="color: red; font-size: 150%;">
    <a
      href='command:katapod.loadPage?[{"step":"step5"}]'
      style="text-decoration: none; cursor: none;"
    >Clicking on this paragraph is a weird way to go back to previous step.</a>
  </p>
</div>

Just keep in mind that the Katapod engine will not inspect the HTML (for example,
you won't have properly-styled tables or embedded from-repo images out-of-the-box).

#### Custom navigation

You can even plan a nonlinear step sequence for your scenario, and design navigation
accordingly. Here we pretend the following step can be done in two ways:

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
  <a title="Back" href='command:katapod.loadPage?[{"step":"step5"}]' class="btn btn-dark navigation-bottom-left">
    ⬅️ Back
  </a>
  <a title="Next (Astra DB)" href='command:katapod.loadPage?[{"step":"step7-astra"}]' 
    class="btn btn-dark navigation-top-right"
    style="margin-left: 8px;"
  >
    Next (Astra DB) ➡️
  </a>
  <a title="Next (Cassandra)" href='command:katapod.loadPage?[{"step":"step7-cassandra"}]' class="btn btn-dark navigation-top-right">
    Next (Cassandra) ➡️
  </a>
</div>
