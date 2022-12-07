<!-- TOP -->
<div class="top">
  <img src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-logo.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">Multi Terminal Scenario</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span>
  </div>
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"step1-astra"}]'
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 2 of 2</span>
 <a href='command:katapod.loadPage?[{"step":"finish"}]' 
    class="btn btn-dark navigation-top-right">End ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">This is it</div>

✅ Observe that, upon loading of this step, a command is triggered on the second terminal.
**But only the first time you get here**.

✅ Ready for a two-line non-executable code block?
```
### {"execute": false}
echo \
  "wow"
```

✅ This code block will *automatically* issue a Ctrl-C, followed by more stuff:
```
### {"terminalId": "term_3", "macrosBefore": ["ctrl_c"]}
# (a Ctrl-C to stop the running process, then:)
find -name "*.md"
```


<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"step1-astra"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"finish"}]'
    class="btn btn-dark navigation-bottom-right">End ➡️
  </a>
</div>
