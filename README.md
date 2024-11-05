# GoogleConsentModeUCP

### Advanced Google Consent Mode

1. Create a notice at https://privacy.evidon.com.

   a. Please ensure that **Google Analytics** vendor is added to the notice disclosure to enable consent updates to the **analytics_storage** consent type.

   b. Pleas ensure that one the following Vendors is added to the notice disclosure to enable consent updates to **ad_storage**, **ad_personalization**, and **ad_user_data**:

    - Google AdSense
    - DoubleClick
    - DoubleClick Bid Manager (formerly Invite Media)
    - Channel Intelligence (Google)
    - AdMeld (Google)
    - Google AdWords
    - Google Display Network
    - AdMob (Google)
    - Google Attribution 360 (formerly Adometry)
    - Google Tag Manager
    - Google Ad Services
    - Google Mobile Ads
    - Google IMA
    - Google Ads
    - Google Analytics

3. Install the Evidon Universal consent Platform GTM template from the Google's Community Template Gallery in GTM.

4. Add the Evidon Universal Consent Platform tag under the "Tag" section in GTM.

    - (Optional) Enable URL passthrough.
   
    - (Optional) Enable Debug mode.

5. Configure the GTM container with the Company ID that has been assigned to your account.

6. Configure the Default consent state. This is the default state of the Google Consent types before a consent update is sent by UCP.

7. Configure the regions where you would like to enabled Advanced Google Consent Mode.

8. Add the "Consent Initialization - All Pages" trigger to the tag. 