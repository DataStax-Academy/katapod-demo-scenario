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
  <a title="Back" href='command:katapod.loadPage?[{"step":"step2"}]' class="btn btn-dark navigation-top-left">
    ⬅️ Back
  </a>
  <span class="step-count">Step 3</span>
  <a title="Next" href='command:katapod.loadPage?[{"step":"step-number-four"}]' class="btn btn-dark navigation-top-right">
    Next ➡️
  </a>
</div>

<!-- CONTENT -->
<div class="step-title">More code-blocks</div>

This is a non-executable code block:

```
### {"execute": false}
echo \
    "wow"
```

Custom background color:

```
### {"terminalId": "term_3", "backgroundColor": "#F0C0C0"}
echo "This block has a weird color."
```

Non-executable and custom background at the same time:

```
### {"execute": false, "backgroundColor": "#B0B9B4"}
CREATE TABLE ...
```

### Handling overflow

Overflowing blocks get a scroll bar:

```
### {"execute": false}
echo This will never be executed, This will never be executed, This will never be executed, This will never be executed, This will never be executed, This will never be executed
    ... did I mention this is not executable?... did I mention this is not executable?... did I mention this is not executable?... did I mention this is not executable?... did I mention this is not executable?... did I mention this is not executable?...
        Oh, yes, this is not an executable code block. Oh, yes, this is not an executable code block. Oh, yes, this is not an executable code block. Oh, yes, this is not an executable code block. Oh, yes, this is not an executable code block.
```

```
echo This is a click-to-execute command, This is a click-to-execute command, This is a click-to-execute command, This is a click-to-execute command, This is a click-to-execute command
```

```
### {"backgroundColor": "#D0F0D0"}
echo This is a custom-background command, This is a custom-background command, This is a custom-background command, This is a custom-background command, This is a custom-background command
```

```
### {"backgroundColor": "#FFF0D0", "execute": false}
echo This is a custom-background nonexecutable command, This is a custom-background nonexecutable command, This is a custom-background nonexecutable command
```

### Syntax highlighting

All common syntax highlighting specifiers are supported, plus `cql`
(which in reality is an alias for `sql` for the time being).

Python:

```python
### {"execute": false}
def myFun(arg):
  minVal = 123
  if arg >= minVal:
    return arg
  else:
    return None
```

Bash (we made this executable so you can run it in your shell):

```bash
for i in `ls *.md`; do
   fname=${i/.md/ Dot Markdown};
   echo "I also found $fname";
done
```

CQL:

```cql
### {"execute": false}
SELECT * FROM table
  WHERE column = 123;

CREATE TABLE table (
  pk INT,
  co TEXT,
  va TIMESTAMP,
  PRIMARY KEY ( ( pk ), co)
) WITH CLUSTERING ORDER BY (co ASC);
```

<!-- NAVIGATION -->
<div id="navigation-bottom" class="navigation-bottom">
  <a title="Back" href='command:katapod.loadPage?[{"step":"step2"}]' class="btn btn-dark navigation-bottom-left">
    ⬅️ Back
  </a>
  <a title="Next" href='command:katapod.loadPage?[{"step":"step-number-four"}]' class="btn btn-dark navigation-bottom-right">
    Next ➡️
  </a>
</div>
