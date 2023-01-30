<!-- TOP -->
<div class="top">
  <img class="scenario-academy-logo" src="https://datastax-academy.github.io/katapod-shared-assets/images/ds-academy-2023.svg" />
  <div class="scenario-title-section">
    <span class="scenario-title">Multi Terminal Scenario</span>
    <span class="scenario-subtitle">ℹ️ For technical support, please contact us via <a href="mailto:aleksandr.volochnev@datastax.com">email</a> or <a href="https://dtsx.io/aleks">LinkedIn</a>.</span>
  </div>
</div>

<!-- NAVIGATION -->
<div id="navigation-top" class="navigation-top">
 <a href='command:katapod.loadPage?[{"step":"intro"}]' 
   class="btn btn-dark navigation-top-left">⬅️ Back
 </a>
<span class="step-count"> Step 1 of 2</span>
 <a href='command:katapod.loadPage?[{"step":"step2"}]' 
    class="btn btn-dark navigation-top-right">Next ➡️
  </a>
</div>

<!-- CONTENT -->

<div class="step-title">Connect to Astra DB and create a database</div>

✅ Notice that on loading of this page a command is executed on the `cqlsh-editor` console.


✅ Run a command implicitly on the first terminal
```
date
```

✅ Also a moot `### ` line would not create trouble
```
###     
time date  # See what I did there?
```

✅ For multiple `### ` lines, the last wins
```
### {"whatever": 123}
echo "Nyvpr fraqf frperg zrffntr gb Obo." | tr 'a-zA-Z' 'n-za-mN-ZA-M'
### cqlsh
```

✅ Run a command on a second terminal (explicitly specified with the `### termTwo` directive)
```
### termTwo
whoami
```

✅ Run another on the first term explicitly (`### cqlsh` directive in code block)
```
###    {"terminalId": "cqlsh", "maxInvocations": 2}
ls -a &
```

Try runnig it a _second_ time. All good? I bet you cannot run it a _third_ time, though. Go ahead, try it again. LOL.

✅ Start Python:

```
### term_3
python
```

✅ How about running code _that does not terminate_? (Scary, I know)
```python
### term_3
import time
i = 0
while True:
   print('Zero & %i' % i)
   i += 1
   time.sleep(0.5)

```



<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
 <a href='command:katapod.loadPage?[{"step":"intro"}]'
   class="btn btn-dark navigation-bottom-left">⬅️ Back
 </a>
 <a href='command:katapod.loadPage?[{"step":"step2"}]'
    class="btn btn-dark navigation-bottom-right">Next ➡️
  </a>
</div>

