---
ticker: AAPL
scale: Logarithmic
chartType: Area
---

```dataviewjs
await dv.el("div", "", { cls: "stock-container" });

const container = document.querySelectorAll('.stock-container')[0];
const ticker = `${dv.current().file.frontmatter.ticker}`;
const scale = `${dv.current().file.frontmatter.scale}`;
const chartType = `${dv.current().file.frontmatter.chartType}`;

const embedUrl = `https://s.tradingview.com/embed-widget/symbol-overview/?locale=en#%7B%22symbols%22%3A%5B%5B%22` + `${ticker}` + `%7C1D%22%5D%5D%2C%22chartOnly%22%3Afalse%2C%22width%22%3A%22100%25%22%2C%22height%22%3A%22100%25%22%2C%22colorTheme%22%3A%22dark%22%2C%22showVolume%22%3Afalse%2C%22showMA%22%3Afalse%2C%22hideDateRanges%22%3Afalse%2C%22hideMarketStatus%22%3Atrue%2C%22hideSymbolLogo%22%3Afalse%2C%22scalePosition%22%3A%22right%22%2C%22scaleMode%22%3A%22` + `${scale}` + `%22%2C%22fontFamily%22%3A%22-apple-system%2C%20BlinkMacSystemFont%2C%20sans-serif%22%2C%22fontSize%22%3A%2212%22%2C%22noTimeScale%22%3Afalse%2C%22valuesTracking%22%3A%221%22%2C%22changeMode%22%3A%22price-and-percent%22%2C%22chartType%22%3A%22` +  `${chartType}` + `%22%2C%22fontColor%22%3A%22rgba(100%2C%20100%2C%20100%2C%20.8)%22%2C%22backgroundColor%22%3A%22rgba(0%2C%200%2C%200%2C%200)%22%2C%22widgetFontColor%22%3A%22rgba(150%2C%20150%2C%20150%2C%200.8)%22%2C%22gridLineColor%22%3A%22rgba(200%2C%20200%2C%20200%2C%200.06)%22%2C%22lineWidth%22%3A2%2C%22lineType%22%3A0%2C%22dateRanges%22%3A%5B%221d%7C1%22%2C%221m%7C30%22%2C%223m%7C60%22%2C%2212m%7C1D%22%2C%2260m%7C1W%22%2C%22all%7C1M%22%5D%2C%22dateFormat%22%3A%22dd%20MMM%20'yy%22%2C%22timeHoursFormat%22%3A%2224-hours%22%7D`

container.innerHTML = `<iframe class="stock-chart" src="${embedUrl}"></iframe>`;
await dv.el("div", container);
```
