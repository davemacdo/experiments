## Bookmarklets

<h3><a href="javascript:(function() {   var currentUrl = window.location.href;   var urlParts = currentUrl.split('/');   var subdomain = urlParts[2].replace(/\./g, '-');   window.location.href = 'https://' + subdomain + '.proxy.wichita.edu/' + urlParts.slice(3).join('/'); })();">read via WSU</a></h3>
