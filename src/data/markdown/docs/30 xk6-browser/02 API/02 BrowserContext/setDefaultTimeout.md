---
title: 'setDefaultTimeout(timeout)'
excerpt: 'Sets the default timeout in milliseconds.'
---

<Blockquote mod="attention">

This feature has **known issues**. For details, refer to
[#456](https://github.com/grafana/xk6-browser/issues/456).

</Blockquote>

Sets the default maximum timeout for all methods accepting a `timeout` option in milliseconds.

| Parameter | Type   | Default                  | Description                  |
|-----------|--------|--------------------------|------------------------------|
| timeout   | number | Dependent on the action. | The timeout in milliseconds. |


### Example

<CodeGroup labels={[]}>

<!-- eslint-skip -->

```javascript
const context = browser.newContext();
context.setDefaultTimeout(1000); // 1s
const page = context.newPage();
page.click('h2'); // times out
```

</CodeGroup>
