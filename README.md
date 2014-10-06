## What it is

Generates Nitrogen erlang terms from HTML.  Useful for converting projects to Nitrogen.

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

## Usage

```sh
make install # sudo
nitrify test/test.html
```

