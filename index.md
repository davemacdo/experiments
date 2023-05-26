## Bookmarklets

Bookmarklets are neat. Install them by dragging the link into your browser's bookmarks bar. 

### Read via WSU

This bookmark will redirect you to your current page through the WSU Libraries proxy service. This should work on- or off-campus and will require you to log in. You will see when logging in that you are doing so on a WSU page, and this bookmarklet does _not_ access your login information. Once you have installed it, the next time you find yourself at a paywalled site that WSU Libraries pays for (like _Chronicle of Higher Ed_), just click the "read via WSU" bookmarklet to be redirected to the same page via the WSU proxy server. Created in collaboration with ChatGPT ([transcript](https://sharegpt.com/c/dxe6gPo)).

<strong><a href="javascript:(function() {     var url = window.location.href;     var protocol = url.split('://')[0];     var rest = url.split('://')[1];     var domain = rest.split('/')[0];     var path = rest.split('/').slice(1).join('/');     var domainParts = domain.split('.');     var tld = domainParts[domainParts.length - 1];     var sld = domainParts.slice(0, -1).join('-');     var newUrl = protocol + '://' + sld + '-' + tld + '.proxy.wichita.edu/' + path;     window.location.href = newUrl; })();">read via WSU</a></strong>

### "Crypto" means "Pretend"

It does what it says. If you're reading an article about pretend money. This will make it more straightforward. 

<strong><a href="javascript:(function() {     function traverse(node) {         if (node.nodeType === Node.TEXT_NODE) {             node.textContent = node.textContent.replace(/crypto/gi, function(match) {                 return match.charAt(0) === 'C' ? 'Pretend' : 'pretend';             });         } else {             node.childNodes.forEach(traverse);         }     }     traverse(document.body); })();">crypto=pretend</a></strong>
