# GoogleConsentModeUCP

## Advanced Google Consent Mode

1. Create a notice at https://privacy.evidon.com.

2. Install the Evidon Universal consent Platform GTM template from the Google's Community Template Gallery in GTM.

3. Add the Evidon Universal Consent Platform tag under the "Tag" section in GTM.

    3a. Enable URL passthrough.
    3b. Enable Debug mode.

4. Configure the GTM container with the Company ID that has been assigned to your account.

5. Configure the Default consent state. This is the default state of the Google Consent types before a consent update is sent by UCP.

6. Configure the regions where you would like to enabled Advanced Google Consent Mode.

7. Add the "Consent Initialization - All Pages" trigger to the tag. 
