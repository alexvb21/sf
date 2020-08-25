# sf

<html>
	<head>
	<meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
	</head>
	<body>
	<style type='text/css'>
	.embeddedServiceHelpButton .helpButton .uiButton {
		background-color: #005290;
		font-family: "Salesforce Sans", sans-serif;
	}
	.embeddedServiceHelpButton .helpButton .uiButton:focus {
		outline: 1px solid #005290;
	}
	@font-face {
		font-family: 'Salesforce Sans';
		src: url('https://c1.sfdcstatic.com/etc/clientlibs/sfdc-aem-

master/clientlibs_base/fonts/SalesforceSans-Regular.woff') format('woff'),
		url('https://c1.sfdcstatic.com/etc/clientlibs/sfdc-aem-master/clientlibs_base/fonts/SalesforceSans-

Regular.ttf') format('truetype');
	}
</style>

<script type='text/javascript' src='https://service.force.com/embeddedservice/5.0/esw.min.js'></script>
<script type='text/javascript'>
	var initESW = function(gslbBaseURL) {
		embedded_svc.settings.displayHelpButton = true; //Or false
		embedded_svc.settings.language = ''; //For example, enter 'en' or 'en-US'

		embedded_svc.settings.defaultMinimizedText = 'TESTS'; //(Defaults to Chat with an Expert)
		embedded_svc.settings.disabledMinimizedText = 'OFF'; //(Defaults to Agent Offline)

		embedded_svc.settings.loadingText = ''; //(Defaults to Loading)
		//embedded_svc.settings.storageDomain = 'yourdomain.com'; //(Sets the domain for your 

deployment so that visitors can navigate subdomains during a chat session)

		// Settings for Chat
		//embedded_svc.settings.directToButtonRouting = function(prechatFormData) {
			// Dynamically changes the button ID based on what the visitor enters in the pre-chat 

form.
			// Returns a valid button ID.
		//};
		//embedded_svc.settings.prepopulatedPrechatFields = {}; //Sets the auto-population of pre-chat 

form fields
		//embedded_svc.settings.fallbackRouting = []; //An array of button IDs, user IDs, or userId_buttonId
		//embedded_svc.settings.offlineSupportMinimizedText = '...'; //(Defaults to Contact Us)

		embedded_svc.settings.enabledFeatures = ['LiveAgent'];
		embedded_svc.settings.entryFeature = 'LiveAgent';

		embedded_svc.init(
			'https://ap4.salesforce.com',
			'https://alexbalurantrailhead-developer-edition.ap4.force.com',
			gslbBaseURL,
			'00D6F000001bhMY',
			'new_snap_in',
			{
				baseLiveAgentContentURL: 'https://c.la1-c2-

ukb.salesforceliveagent.com/content',
				deploymentId: '5726F0000000OSA',
				buttonId: '5736F0000000NAg',
				baseLiveAgentURL: 'https://d.la1-c2-ukb.salesforceliveagent.com/chat',
				eswLiveAgentDevName: 

'EmbeddedServiceLiveAgent_Parent04I6F000000TN78UAG_16b43928885',
				isOfflineSupportEnabled: false
			}
		);
	};

	if (!window.embedded_svc) {
		var s = document.createElement('script');
		s.setAttribute('src', 'https://ap4.salesforce.com/embeddedservice/5.0/esw.min.js');
		s.onload = function() {
			initESW(null);
		};
		document.body.appendChild(s);
	} else {
		initESW('https://service.force.com');
	}
</script>
	</body>
</html>
