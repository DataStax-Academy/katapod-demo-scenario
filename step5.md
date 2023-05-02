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
  <a title="Back" href='command:katapod.loadPage?[{"step":"step-number-four"}]' class="btn btn-dark navigation-top-left">
    ⬅️ Back
  </a>
  <span class="step-count">Step 5</span>
  <a title="Next" href='command:katapod.loadPage?[{"step":"step6"}]' class="btn btn-dark navigation-top-right">
    Next ➡️
  </a>
</div>

<!-- CONTENT -->
<div class="step-title">More style, fancy stuff</div>

## Collapsible blocks

This is the main text. Now a collapsed, expandable block comes:

<details class="katapod-details"><summary>Click for gauge bosons</summary>

1. Gluon
2. Photon
3. W boson
4. Z boson

You should leave blank lines after the `<details ...` line and before the
`</details>` line for the markdown to render in the block.

Also don't forget to use the `katapod-details` class name here.

</details>

## Tables

Standard Markdown tables are supported:

| Spider genus | Family |
|--------|--------|
| Steatoda | Theridiidae |
| Gibbaranea | Araneidae |
| Heliophanus | Salticidae |
| Eratigena | Agelenidae |

## Images

You can embed images with HTML `<img>` tags if you want, which will work only with absolute paths:

<img src="https://raw.githubusercontent.com/DataStax-Academy/katapod-quickstart/main/images/images/fishes_1.png" />

To embed images in the repo itself, use Markdown image syntax, either with a leading slash:

![Fishes two](/images/fishes_2.png)

or without:

![Fishes three](images/fishes_3.png)

## Links

Markdown links work as expected: [example](https://github.com/DataStax-Academy/katapod-quickstart)

**Note**: usually you should warn users to check their popup blocker to make sure the new tab gets opened.
This cannot be bypassed since it comes from the Gitpod layer doing its policing.

#### Lab-specific URLs

Sometimes your Katapod lab runs a service that you later have to reach on a specific port.
You can use the special `gp url` command to get the full URL to the service: for instance,
instructions to open a container running Grafana might be:

_While generally it would be reached on port 3000 at your monitoring instance's address, **within this learning environment** you can directly open it in a new browser tab by running the command:_

```bash
### cqlsh
MONITORING_URL=`gp url 3000`
echo "Opening ${MONITORING_URL} ..."
gp preview --external ${MONITORING_URL}
```

_(Depending on your browser and popup-blocker settings, chances are no tab will open at this point. In that case, simply grab the URL output on your console and manually point a new tab to that address.)_

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
  <a title="Back" href='command:katapod.loadPage?[{"step":"step-number-four"}]' class="btn btn-dark navigation-bottom-left">
    ⬅️ Back
  </a>
  <a title="Next" href='command:katapod.loadPage?[{"step":"step6"}]' class="btn btn-dark navigation-bottom-right">
    Next ➡️
  </a>
</div>
