- [クリックした要素のXPathを表示](javascript: function getXpath(a) { if (a && a.parentNode) { for (var d = getXpath(a.parentNode) + "/" + a.tagName, c = [], b = 0; b < a.parentNode.childNodes.length; b++) { var e = a.parentNode.childNodes[b]; e.tagName == a.tagName && c.push(e) } if (1 < c.length) for (b = 0; b < c.length; b++)if (c[b] === a) { d += "[" + (b + 1) + "]"; break } return d.toLowerCase() } return "" } document.addEventListener("click", function (a) { alert(getXpath(a.target)) });)