## What it is

nitrify will generate valid Nitrogen erlang code from HTML.  Useful for converting existing projects to nitrogen.

## Usage

    ./nitrify test/test.html

## What it does

Input

```html
<div class="popup-email">
  <div class="element"> 
    text1
    <button id="btn" class="btn medium" type="button">OK</button>
    text2
  </div>
</div>
```

Output

```erlang
#panel {
  class = "popup-email",
  body = [
    #panel {
      class = "element",
      body = [
        "text1",
        #button {
          html_id = "btn",
          class = "btn medium",
          body = [
            "OK"
          ]
        },
        "text2"
      ]
    }
  ]
}.
```
