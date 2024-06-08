# CSS Battle

We're doing a battle together at https://cssbattle.dev/

## Daily Target

We did this target: https://cssbattle.dev/play/WkQVfaBd5YZAxAAgmtWt

<details>
<summary>Solution</summary>

```html
<style>
  * {
    background: radial-gradient(circle, #085328 55px, #1F7D3B 0 85px, #2F9947 0 115px, #49C85B 0);
  }
</style>
```
</details>

## Target 153

https://cssbattle.dev/play/153

- in the daily battle, we could write a solution using no HTML and apply the styles directly on the `*` CSS Selector
- for the battle 153, we needed another solution. First, similarly, we applied some styles to the body:
- Then, we thought about nesting divs, such as:
  ```
  <div>
    <div></div>
    <div></div>
  </div>
  ```
  and then repeating a pattern, e.g. one pattern background square and one with a circle
- We learned tricks to reduce characters a lot, which you probably wouldn't do in production code ;)
- Example `<div s>` and CSS `[s] {}` to prevent spending characters by adding the class attributes and class names.
- And then Jörn showed us tricks such as `background: conic-gradient(#E3516E 25%, #FADE8B 0 50%, #E3516E 0 75%, #FADE8B 0) 0 0 / 80px 80px);`


<details>
<summary>Checkerboard</summary>

```html
<div></div>
<style>
  body {
    display: grid;
    place-items: center;
    background: #E3516E;
  }
  div {
    width: 200px;
    height: 200px;
    background:
      radial-gradient(circle at 60px 100px, #E3516E 10px, #0000 0) 0 0 / 80px 200px,
      radial-gradient(circle at 20px 60px, #FADE8B 10px, #0000 0) 0 0 / 80px 80px,
      radial-gradient(circle at 60px 20px, #FADE8B 10px, #0000 0) 0 0 / 80px 80px,
      conic-gradient(#E3516E 25%, #FADE8B 0 50%, #E3516E 0 75%, #FADE8B 0) 0 0 / 80px 80px;
  }
</style>
```
</details>
