# GoogleConsentModeUCP

### Notice Configuration

1. Create a notice at https://privacy.evidon.com

   * Please ensure that **Google Analytics** vendor is added to the notice disclosure to enable consent updates to the **analytics_storage** consent type.

   * Pleas ensure that one the following Vendors is added to the notice disclosure to enable consent updates to **ad_storage**, **ad_personalization**, and **ad_user_data**:

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

![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/NoticeDisclosure.png?raw=true)

    Relevant Documentation:

        - https://community.crownpeak.com/t5/Universal-Consent-Platform-UCP/Universal-Consent-Platform-Getting-Started-Guide/ta-p/7756




### Advanced Google Consent Mode

1. Install the Evidon Universal consent Platform GTM template from the Google's Community Template Gallery in GTM.

![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/CommunityGallary.png?raw=true)

2. Add the Evidon Universal Consent Platform tag under the "Tag" section in GTM.

![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/AddingNewTag.png?raw=true)

3. Configure the GTM container with the Company ID that has been assigned to your account.

4. (Optional) Enable URL passthrough.
   
5. (Optional) Enable Debug mode.

6. Ensure that the option to enable Advanced Google consent mode is checked.

7. Configure the Default consent state for each consent type (ad_storage, ad_personalization, ad_user_data, and analytics_storage). This is the default state of the consent types if the end user has not provided consent.

8. Configure the regions where you would like to enabled Advanced Google Consent Mode.

![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/AdvancedConsentMode.png?raw=true)

9. Add the "Consent Initialization - All Pages" trigger to the tag.

    *Relevant Documentation:

        - https://support.google.com/google-ads/answer/10000067?hl=en

### Basic Google Consent Mode

1. Install the Evidon Universal consent Platform GTM template from the Google's Community Template Gallery in GTM.

![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/CommunityGallary.png?raw=true)

2. Add the Evidon Universal Consent Platform tag under the "Tag" section in GTM.

![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/AddingNewTag.png?raw=true)

3. Configure the GTM container with the Company ID that has been assigned to your account.

4. (Optional) Enable URL passthrough.
   
5.  (Optional) Enable Debug mode.

6. Disable Advanced Google Consent Mode.

![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/BasicConsentMode.png?raw=true)

7. Add the "Consent Initialization - All Pages" trigger to the tag.

    *Relevant Documentation:

        - https://support.google.com/google-ads/answer/10000067?hl=en





### Tag Wrapping

Tag Wrapping is only necessary for non-google tags when Advanced Google consent mode is enabled; Google tags will need to be fired after the default consent is set. Please enable the debug mode to see if any Google tags are accessing the **dataLayer** object before the default consent state is defined. If Advanced Google Consent mode is not enabled, then all tags will need to be fired with Evidon triggers.

1. Download the GTM Recipe available at https://privacy.evidon.com.

    * Please ensure that the consent level is set to "Category".

![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/GTMRecipe.png?raw=true)

2. Import the GTM recipe into your GTM container without overwriting changes. This file will contain the triggers needed for Tag Wrapping.

![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/ImportingTriggers.png?raw=true)

3. Please attach a "{Category Name} Consented Trigger" and the "All Categories Consented Trigger" to each tag you plan to fire with user consent. If you have triggers already configured for your tags, please create a trigger group with one of the category triggers; both condition will need to be true for the tag to fire. All Evidon triggers will fire on the following event **evidonConsentGiven**. 

Tag Wrapping a tag with triggers:


![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/exampleTriggers.png?raw=true)

Tag Wrapping with a trigger Group:


![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/TriggerGroup1.png?raw=true)


![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/TriggerGroup2.png?raw=true)


![alt text](https://github.com/justindeng21/GoogleConsentModeUCP/blob/main/images/TriggerGroup3.png?raw=true)
