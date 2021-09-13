<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [puppeteer](./puppeteer.md) &gt; [ElementHandle](./puppeteer.elementhandle.md) &gt; [type](./puppeteer.elementhandle.type.md)

## ElementHandle.type() method

Focuses the element, and then sends a `keydown`, `keypress`/`input`, and `keyup` event for each character in the text.

To press a special key, like `Control` or `ArrowDown`, use [ElementHandle.press()](./puppeteer.elementhandle.press.md).

<b>Signature:</b>

```typescript
type(text: string, options?: {
        delay: number;
    }): Promise<void>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  text | string |  |
|  options | { delay: number; } |  |

<b>Returns:</b>

Promise&lt;void&gt;

## Example 1


```js
await elementHandle.type('Hello'); // Types instantly
await elementHandle.type('World', {delay: 100}); // Types slower, like a user

```

## Example 2

An example of typing into a text field and then submitting the form:

```js
const elementHandle = await page.$('input');
await elementHandle.type('some text');
await elementHandle.press('Enter');

```
