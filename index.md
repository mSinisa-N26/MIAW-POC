<html>
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Messaging POC</title>
    <!-- <link rel="stylesheet" href="./style.css">
    <link rel="icon" href="./favicon.ico" type="image/x-icon"> -->
  </head>
 <body> 

<script type='text/javascript'>
	window.addEventListener("onEmbeddedMessagingReady", e => {
        console.log("onEmbeddedMessagingReady event triggered");
        //embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields({
        //    "language" : "ES",
        //    "userId" : "1234567890ABCDEFG"
        //});
	});
	console.log("hidden fields set");
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'es'; // For example, enter 'en' or 'en-US'

			embeddedservice_bootstrap.init(
				'00D9O000007kCYP',
				'GitHub_Messaging_POC',
				'https://n26--chatpoc.sandbox.my.site.com/ESWGitHubMessagingPOC1727961737610',
				{
					scrt2URL: 'https://n26--chatpoc.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://n26--chatpoc.sandbox.my.site.com/ESWGitHubMessagingPOC1727961737610/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
  </body>
</html>
