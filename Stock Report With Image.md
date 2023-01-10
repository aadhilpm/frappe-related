---
share: true
---

```javascript

var intervalId = window.setInterval(function () {
  populate_images();
}, 1000);

function populate_images() {
  // This assumes the images go into the first

  column.$(".dt-cell__content--col-1").map(function (i, el) {
    var content = $(el).html().trim();
    if (content.charAt(0) === "/") {
      $(el).html('<img src="' + content + '">');
    }
  });
}



```


https://discuss.erpnext.com/t/stock-report-with-image/55832/3