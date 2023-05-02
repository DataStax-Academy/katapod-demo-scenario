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
  <a title="Back" href='command:katapod.loadPage?[{"step":"intro"}]' class="btn btn-dark navigation-top-left">
    ⬅️ Back
  </a>
  <span class="step-count">Step 1</span>
  <a title="Next" href='command:katapod.loadPage?[{"step":"step2"}]' class="btn btn-dark navigation-top-right">
    Next ➡️
  </a>
</div>

<!-- CONTENT -->
<div class="step-title">Running commands</div>

This scenario is configured with three consoles.

Consoles, scripts and most other scenario properties are set in file `.katapod-config.json`.

Katapod can execute commands (on a target console) in two ways:

- when certain pages are loaded and rendered;
- when the user clicks on command code blocks.

The welcome messages on the first two consoles are the result of scripts being executed
upon loading of `intro.md`. This is the (fixed) name of the entry-point page.

Clicking on an executable code block launches the command in a console. This clears
the second console:

```
### termTwo
clear
```

Do the same with the first console:

```
clear
```

Commands can bear a specification of how many times they are allowed to be run.
For example, the message on the first console for the intro-page has `"maxInvocations": 2`.
The intro-page-load for the second console triggers _two_ commands,
the first implicitly with the default of executing only once,
the second with `"maxInvocations": "unlimited"`.

✅ Try going to the intro to check what gets executed again. Then come back here.

✅ Now clear the consoles and go once more to the intro. What command ran only once? Twice? Forever?

## Executing code blocks

_Note: keep the source code for the scenario at hand to make sense of what you do!_

Code blocks on the page are executed with a click on them.

```
### term_3
echo "Third terminal."
```

"Naked" code blocks implicitly run on the first terminal

```
date
```

You specify the target terminal by putting a line in the code block which starts with `### ` (note the space after the pounds),
followed by the terminal ID:

```
### termTwo
echo "Second terminal."
```

Moot `### ` lines do no harm:

```
###     
date
```

When there are multiple `### ` lines, the last wins:

```
### term_3
echo "Nyvpr fraqf frperg zrffntr gb Obo." | tr 'a-zA-Z' 'n-za-mN-ZA-M'
### cqlsh
```

The `### termTwo` syntax is actually shorthand for `### {"terminalId": "termTwo"}`. So this:

```
### termTwo
whoami
```

is equivalent to this:

```
### {"terminalId": "termTwo"}
whoami
```

### More command behaviour

Run this command on the first terminal:

```
###    {"terminalId": "cqlsh", "maxInvocations": 2}
ls scenario_scripts
```

Try runnig it a _second_ time. All good? I bet you cannot run it a _third_ time, though. Try it.
(You may have guessed by now that the default number of invocations for in-page code blocks is "unlimited").

Start Python on the third terminal:

```
### term_3
python
```

This command launches a loop that will go on forever (note a newline at the end for the Python REPL to start looping):

```
### term_3
import time
i = 0
while True:
   print('Looping ... %i' % i)
   i += 1
   time.sleep(0.5)

```

Good news: you can inject a `Ctrl-C` right before executing another command.
The following block, indeed, will send a `Ctrl-C` to the loop to stop it,
then will exit the Python REPL and run a shell command:

```
### {"terminalId": "term_3", "macrosBefore": ["ctrl_c"]}
# (a Ctrl-C to stop the running loop, then:)
exit()

# we're back to the shell:
date +"%Y-%m-%d"
```

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
  <a title="Back" href='command:katapod.loadPage?[{"step":"intro"}]' class="btn btn-dark navigation-bottom-left">
    ⬅️ Back
  </a>
  <a title="Next" href='command:katapod.loadPage?[{"step":"step2"}]' class="btn btn-dark navigation-bottom-right">
    Next ➡️
  </a>
</div>
