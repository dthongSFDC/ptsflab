Set Up Sales Cloud Einstein
Salesforce, Spring ’26
Last updated: March 31, 2026

© Copyright 2000–2026 Salesforce, Inc. All rights reserved. Salesforce is a registered trademark of Salesforce, Inc., as are other
names and marks. Other marks appearing herein may be trademarks of their respective owners.

CONTENTS
Sales Cloud Einstein . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 1
Prepare for Sales Cloud Einstein . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2
Data Requirements for Sales Cloud Einstein . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 2
Sales Cloud Einstein and Sandbox . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 3
Run the Sales Cloud Einstein Readiness Assessor . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 5
Considerations for Setting Up Sales Cloud Einstein. . . . . . . . . . . . . . . . . . . . . . . . . . . . 7
Considerations for Setting Up Einstein Automated Contacts . . . . . . . . . . . . . . . . . . . . . . . . . 8
Considerations for Setting Up Einstein Lead Scoring. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 9
Considerations for Setting Up Einstein Opportunity Scoring . . . . . . . . . . . . . . . . . . . . . . . . . 10
Considerations for Setting Up Einstein Forecasting . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 11
Set Up Sales Cloud Einstein . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 13
Select Who Can Use Sales Cloud Einstein . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 14
Access the Sales Cloud Einstein Setup Assistant. . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 15
Enable Einstein Automated Contacts . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 15
Enable Einstein Lead Scoring . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 16
Enable Einstein Opportunity Scoring . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 18
Enable Einstein Forecasting . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20
Troubleshoot Sales Cloud Einstein Setup Errors . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . . 20

SALES CLOUD EINSTEIN
Sales Cloud Einstein is like having your own data scientist within Salesforce. Einstein learns from your team’s sales activities and CRM
data, and then gives you intelligent insights and predictive scoring to help you grow your pipeline fast. Sales Cloud Einstein also helps
you increase sales productivity with machine learning and business sentiment analysis.
To get a better understanding of what’s offered with Sales Cloud Einstein, review Sales Cloud Einstein in Salesforce Help, and work with
your Salesforce contact to figure out which features are best for your team.
| Feature | What It Does | How It Helps |
| ------- | ------------ | ------------ |
Einstein Activity Capture Keeps your email and calendar Track sales-related activity on
|     | applications in sync with | records and generate insights. |
| --- | ------------------------- | ------------------------------ |
Salesforce.
Einstein Automated Contacts Finds new contacts and Let reps spend less time on data
|     | opportunity contact roles to add | entry and more time on sales. |
| --- | -------------------------------- | ----------------------------- |
to Salesforce.
Einstein Forecasting Provides predictions about your Improve forecasting accuracy
|     | teams forecasting amount at the | and track how your sales teams |
| --- | ------------------------------- | ------------------------------ |
|     | end of a forecasting period.    | are doing.                     |
Einstein Lead Scoring Scores leads from 1 to 99 based Prioritize leads and determine
|     | on how well they fit your lead | where to focus sales efforts. |
| --- | ------------------------------ | ----------------------------- |
conversion patterns.
Einstein Opportunity Scoring Scores opportunities from 1 to Prioritize opportunities so you
|     | 99 based on how likely they are | can focus on the deals that are |
| --- | ------------------------------- | ------------------------------- |
|     | to close.                       | more likely to close.           |
Einstein Opportunity Insights Provides predictions, smart Use relevant updates to win
|     | follow-ups, and key moments | more deals. |
| --- | --------------------------- | ----------- |
related to opportunities.
| Einstein Account Insights | Highlights key business | Stay informed about      |
| ------------------------- | ----------------------- | ------------------------ |
|                           | developments and key    | developments that affect |
|                           | moments about accounts. | customers.               |
Sales Analytics app Provides dashboards about Evaluate how well various
|     | various Sales Cloud Einstein | Einstein features are working in |
| --- | ---------------------------- | -------------------------------- |
|     | features.                    | your org. For more information,  |
see CRM Analytics for Sales Cloud
Einstein in the Salesforce Help
| Inbox | Integrates email and calendar | Help sales reps boost         |
| ----- | ----------------------------- | ----------------------------- |
|       | with Salesforce.              | productivity and work smarter |
right from their inbox.
For more information, see Inbox
in the Salesforce Help.
1

PREPARE FOR SALES CLOUD EINSTEIN
Before you set up Sales Cloud Einstein feature, review information about data requirements and
EDITIONS
other considerations. Learn about sandbox support and how to run the readiness assessor.
Available in: Lightning
Data Requirements for Sales Cloud Einstein Experience and Salesforce
Classic
To generate the most reliable intelligence, you must meet data requirements for each Sales
Cloud Einstein feature.
Available for an extra cost
Sales Cloud Einstein and Sandbox in: Enterprise, Performance,
and Unlimited Editions
Review which Sales Cloud Einstein features are available in sandbox.
Run the Sales Cloud Einstein Readiness Assessor
Wondering whether you’re ready for Sales Cloud Einstein or whether it can help your sales reps? Run the Sales Cloud Einstein
Readiness Assessor to find out. We analyze your Salesforce implementation, in either a production or sandbox environment, and
then send you a personalized report. The report tells you which Einstein features you’re ready to use now and which ones require
extra steps.
Data Requirements for Sales Cloud Einstein
To generate the most reliable intelligence, you must meet data requirements for each Sales Cloud
EDITIONS
Einstein feature.
Available in: Lightning
Tip: To check whether you meet the data requirements, run the Sales Cloud Einstein Assessor.
Experience and Salesforce
Classic
Einstein Automated Contacts
Available with Sales Cloud
Einstein, which is available
Important: Feature is scheduled for retirement on February 15, 2025. See Einstein Automated in Performance and
Contacts Retirement. Unlimited Editions, and for
an extra cost in Enterprise
• You must have at least 30 business accounts.
Edition
• If you use person accounts, at least 50 percent of accounts must be business accounts.
Einstein Activity Capture
• You must have at least 30 accounts, contacts, leads, or opportunities.
Einstein Lead Scoring
These requirements apply to each segment of leads you create during setup, including the All Leads (Default) segment.
• At least 1,000 leads must be created in the last 200 days.
• Of the leads created in the last 200 days, at least 120 must be converted to an account and contact.
• (Optional) Of the leads created in the last 6 months (180 days), at least 120 must be converted to an account and contact with an
opportunity created at conversion time.
2

Prepare for Sales Cloud Einstein Sales Cloud Einstein and Sandbox
When you score all leads together without creating segments, and you don’t have enough lead conversion data to build your own
predictive model, Einstein uses a global model. The global model uses anonymous data from many Salesforce customers. When you
accumulate enough lead data, Einstein builds a scoring model with your data and uses the model with the better results.
Einstein Opportunity Scoring
• You must have at least 200 closed won opportunities in last 24 months, each with a lifespan of at least 2 days.
• You must have at least 200 closed lost opportunities in last 24 months, each with a lifespan of at least 2 days.
• Opportunity history shows an average of one update to each closed opportunity.
• Use the standard opportunity Stage field because it’s used to calculate win rates, and win rates are used to generate scores. If you
change the names of the opportunity stage picklist values, make sure that the values are mapped to the correct stage type: Open,
Closed/Won. or Closed/Lost.
• If your win rate is extremely high or low, your scores could be skewed. For example, if your win rate is above 90 percent, you could
get a large number of opportunities with scores above 90. To avoid skewed scores, make sure that opportunities are set to the correct
closed stage. (A win rate is calculated by dividing the last two years of closed-won opportunities by all closed opportunities from
that same period.)
If you don’t have enough opportunity data to build your own predictive model, Einstein uses a global model. The global model uses
anonymous data from many Salesforce customers. When you accumulate enough opportunity data, Einstein builds a scoring model
with your data and uses the model with the better results.
Einstein Forecasting
• Salesforce Forecasting must be enabled.
• You must work with opportunities in Salesforce for at least 12 months. Specifically, the opportunity history must show at least one
update in each of the past 12 months.
• You must use a standard fiscal year. Standard fiscal years follow the Gregorian calendar, but can start on the first day of any month
of the year.
• Forecasts must be measured by opportunity revenue. Predictions are generated for only the oldest activated opportunity revenue
forecast type.
• Your forecast hierarchy must include at least one forecasting enabled user who reports to a forecast manager.
• The Amount field should be populated in at least 80 percent of open opportunities.
Sales Cloud Einstein and Sandbox
Review which Sales Cloud Einstein features are available in sandbox.
EDITIONS
Tip:
Available in: Lightning
• A sandbox environment is best suited for testing how Sales Cloud Einstein features work
Experience and Salesforce
with architecture, workflows, and Lightning components. Because the data in a sandbox
Classic
environment is limited, we recommend that you don’t evaluate the performance of the
Einstein model based on what you see in sandbox. Instead, evaluate the model in a Available with Sales Cloud
Einstein, which is available
production org that has the required amount of historical data. You can run the Sales
in Performance, and
Cloud Einstein Assessor in a sandbox to check which Sales Cloud Einstein features are
Unlimited editions, and for
ready to be turned on.
an extra cost in Enterprise
Edition
3

Prepare for Sales Cloud Einstein Sales Cloud Einstein and Sandbox
• Don’t manipulate the sandbox data before running the Einstein readiness assessor. Doing so can result in the assessor incorrectly
passing some of the requirements. For example, Einstein Opportunity Scoring requires opportunities to be at least two days
old and have updates that reflect your actual business process. If your sandbox data doesn’t include opportunity history and
you then update opportunities on the same day that you added them to the sandbox, the assessor incorrectly evaluates the
requirement as met. Then, if you turn on Opportunity Scoring in sandbox, you don’t see scores. If you don’t see scores in
sandbox but believe that you fulfilled all the requirements, contact Salesforce Customer Support.
Feature Sandbox Support Notes
Einstein Lead Scoring Einstein Lead Scoring requires at least six
months of data, so make sure that you
refresh the full sandbox.
Re-enable the feature in each new sandbox
or when a sandbox is refreshed.
Einstein Opportunity Scoring Einstein Opportunity Scoring requires at
least six months of data, so make sure that
you refresh the full sandbox.
If you use Opportunity Scoring without
Performance or Unlimited editions or Sales
Cloud Einstein licenses, sandbox isn’t
supported.
Re-enable the feature in each new sandbox
or when a sandbox is refreshed.
Einstein Activity Capture Because sandbox is best for testing how
Einstein Activity Capture works and how it
looks, no data is copied from production to
sandbox. After you set up Einstein Activity
Capture in sandbox, any refresh of that
sandbox turns off Einstein Activity Capture
and removes all connected accounts from
the sandbox.
Inbox
Recommended Connections Einstein Activity Capture is required.
Einstein Email Insights Einstein Activity Capture is required.
Sales Analytics
Einstein Forecasting Einstein Forecasting requires two years of
data, but sandbox environments support
up to six months of data.
4

Prepare for Sales Cloud Einstein Run the Sales Cloud Einstein Readiness Assessor
Run the Sales Cloud Einstein Readiness Assessor
Wondering whether you’re ready for Sales Cloud Einstein or whether it can help your sales reps?
EDITIONS
Run the Sales Cloud Einstein Readiness Assessor to find out. We analyze your Salesforce
implementation, in either a production or sandbox environment, and then send you a personalized
Available in: Lightning
report. The report tells you which Einstein features you’re ready to use now and which ones require
Experience
extra steps.
Available in: Enterprise,
The Sales Cloud Einstein Readiness Assessor can be run in production and sandbox orgs. Sandbox
Performance, and
is best suited for testing Sales Cloud Einstein features in terms of architecture, workflows, and
Unlimited Editions
Lightning components. Because the data in sandbox is limited, we recommend that you don’t
evaluate the performance of the Einstein model based on what you see in sandbox. Instead, evaluate
USER PERMISSIONS
the model in a production org that has the required amount of historical data.
1. From Setup, enter Assessors in the Quick Find box, and then select Sales Cloud Einstein To run the Sales Cloud
Assessor under Einstein Assessors. Einstein Readiness Assessor:
• Customize Application
2. Fill in the form and click Generate Report. If you’re using a sandbox, click Generate Report
(Sandbox).
Alternatively, you can go directly to the assessor and follow the instructions to let Salesforce access your data.
When the assessment is done, we send you an email to let you know that your personalized Sales Cloud Einstein readiness report is
available from the Files tab in Salesforce.
If you have problems running the readiness assessor, upgrade your browser to the latest version and try again.
Note:
• The Sales Cloud Einstein Readiness assessor isn’t available for Salesforce Government Cloud customers.
• The Sales Cloud Einstein Readiness Assessor accesses Salesforce data from your account, contact, lead, user, and opportunity
records to determine if your Salesforce org meets eligibility requirements for each Sales Cloud Einstein feature. The data, your
administrator email address, and an authentication credential is saved and/or processed by Salesforce technologies built on
Amazon Web Services and Heroku that offer different privacy and security standards. These third-party hosting providers don’t
5

Prepare for Sales Cloud Einstein Run the Sales Cloud Einstein Readiness Assessor
store any personally identifiable information. This data is used to generate your personalized Sales Cloud Einstein Readiness
Report. The authentication credential is deleted and access to your org's data is immediately revoked after the report is
generated.
6

CONSIDERATIONS FOR SETTING UP SALES CLOUD EINSTEIN
Before setting up Sales Cloud Einstein, consider these requirements, limitations, and nuances for
EDITIONS
each feature.
Available in: Lightning
General Considerations Experience and Salesforce
Classic
• Sales Cloud Einstein is available only to users with standard Salesforce licenses. Available with Sales Cloud
Einstein, which is available
• Sales Cloud Einstein isn’t supported in Government Cloud and Government Cloud Plus
in Performance and
organizations. Turning on Sales Cloud Einstein can send data outside the authorization boundary.
Unlimited Editions, and for
Contact your Salesforce account executive for more details.
an extra cost in Enterprise
• When you set up Sales Cloud Einstein, Salesforce installs two packages in your org, SalesforceIQ Edition
Cloud and Sales Insights. Each package adds an associated integration user and profile. Salesforce
uses these entities to provide insights to your org. If you update these entities, it can affect your
org’s ability to get insights. Depending on the Einstein features you turn on, these integration users can have full access to Accounts,
Campaigns, Contacts, Leads, and Opportunities. These users don’t modify your org’s data and don’t affect your Salesforce license
usage.
• Platform encryption isn’t currently supported with Sales Cloud Einstein.
• Some Sales Cloud Einstein features require users to connect a Microsoft® Exchange or Gmail™ account to Salesforce.
• Sales Cloud Einstein included in Sales Cloud Unlimited Edition provides analytics reporting using the CRM Analytics platform. When
using this functionality, your license doesn't allow you to:
– Build custom analytics apps or dashboards
– Upload, access, or connect external data using the API with the exception of datasets provided with Sales Cloud Einstein
– Import data from Salesforce standard or custom objects that aren’t included in this feature
Feature Considerations
• Einstein Lead Scoring
• Einstein Opportunity Scoring
• Einstein Forecasting
• Einstein Activity Capture
• Salesforce Inbox
• Sales Analytics
7

Considerations for Setting Up Sales Cloud Einstein Considerations for Setting Up Einstein Automated Contacts
Considerations for Setting Up Einstein Automated Contacts
Before setting up Einstein Automated Contacts, consider these requirements, limitations, and
EDITIONS
nuances.
Available in: Lightning
Important: Feature is scheduled for retirement on February 15, 2025. See Einstein Automated
Experience
Contacts Retirement.
• You must have at least 30 business accounts. Available with Sales Cloud
Einstein, which is available
• If you use person accounts, at least 50 percent of accounts must be business accounts.
in Performance and
• Einstein Automated Contacts isn’t supported in sandbox environments. Unlimited Editions, and for
• Suggestions are based on data from manually and automatically logged activities. an extra cost in Enterprise
Edition
• Contact suggestions and opportunity contact role suggestions aren’t available in standard
reporting, but you can use them in custom report types.
• To add or decline contact suggestions, users need edit access on accounts.
• To add or decline opportunity contact role suggestions, users need edit access on opportunities, and read or edit access on contacts.
• When an opportunity contact role suggestion refers to a contact that a user doesn’t have access to, the following happens. The user
doesn’t see the suggestion on the opportunity record. When the user views the complete list of suggestions (using the Einstein
Opportunity Contact Role Suggestions item from the App Launcher), we show all suggestions but hide contact fields that the user
doesn’t have access to.
• Make sure that sales reps have access to contact fields, such as Email, Title, or Phone, so that they can see those fields with opportunity
contact role suggestions.
• If required contact fields don’t have a default value, errors can occur when contacts are automatically created. If an error occurs, the
contact is shown to users as a suggestion.
• If the New Contact action for the Contact object is overridden through a custom Visualforce page or Lightning component, then
the Add button on the contact suggestion doesn’t always populate the contact record.
Access Requirements
Users need access to specific opportunity and account fields to see insights everywhere.
• On the Opportunity object, you need the Name and Type fields.
• On the Account object, you need the Activity, Name, Title, and Type fields.
8

Considerations for Setting Up Sales Cloud Einstein Considerations for Setting Up Einstein Lead Scoring
Considerations for Setting Up Einstein Lead Scoring
Before you set up Einstein Lead Scoring, consider these requirements and limitations.
EDITIONS
General Available in: Lightning
Experience and Salesforce
• At least 1,000 leads must be created in the last 200 days. Classic
• Of the leads created in the last 200 days, at least 120 must be converted to an account and Available with Sales Cloud
contact. Einstein, which is available
• (Optional) Of the leads created in the last 6 months (180 days), at least 120 must be converted in Performance and
to an account and contact with an opportunity created at conversion time. Unlimited Editions, and for
an extra cost in Enterprise
These requirements apply to each segment of leads you create during setup, including the All Leads
Edition
(Default) segment.
When you score all leads together without creating segments, and you don’t have enough lead
conversion data to build your own predictive model, Einstein uses a global model. The global model uses anonymous data from many
Salesforce customers. When you accumulate enough lead data, Einstein builds a scoring model with your data and uses the model with
the better results.
• Encourage reps to add as much data to their leads as possible. When leads have more data, Einstein Lead Scoring generates better
insights.
• Reps must have read access to the Company, Phone, and Email fields on leads.
• Don’t install Apex classes that reference the ScoreIntelligence field until after you enable Einstein Lead Scoring and receive the
notification that enablement is complete. Otherwise, references to the ScoreIntelligence field are invalid.
• Einstein does not use encrypted lead fields in lead score analysis. When you turn encryption on or off for a field, Einstein includes
the change in the next analysis. Einstein reanalyzes your leads approximately every 10 days.
• If you have over a million scored leads, the Einstein Lead Scoring Analytics app can stop working. The exact number depends on
your org’s configuration.
• If you turned on Einstein Lead Scoring in Spring ’20 or earlier, you no longer need the Lead filter in the Einstein Lead Scoring Analytics
app. To remove the filter, open the Data Manager in Analytics Studio and then click Connect. Click Lead, then Continue. Remove
the ScoreIntelligence.Score >= 0 filter text and save your changes.
Scoring Leads in Segments
• Data requirements for scoring all leads together also apply to individual lead segments.
• Each time you change Einstein Lead Scoring settings, Einstein updates the segment IDs for each lead segment, even if you score all
your leads in a single segment. During these updates, some data in the CRM Analytics Lead Scoring Dashboard, including lead
conversion rates, can be incorrect until Einstein updates your scores based on the new settings.
• When using segments or any other custom lead scoring settings, any new fields added to leads must be added manually to the list
of included fields for each segment if you Einstein to consider them during scoring.
Using Filters
If you create lead segments using field filters, be aware of what happens when you delete or deactivate picklist field values.
• If you delete a picklist value from a standard field, you can’t use the value to set up a field filter.
9

Considerations for Setting Up Sales Cloud Einstein Considerations for Setting Up Einstein Opportunity Scoring
• If you deactivate a picklist value from a standard field, you can’t use it to set up a field filter. However, existing field filters based on
that value still work with lead records that contain the deactivated value.
• If you create a field filter using a standard field value and then delete that filtered value from the field, the filter still functions correctly.
However, the field appears in Setup with a blank value.
• If you delete a picklist value from a custom field, it still appears in Setup, but any filter created with that value doesn’t function.
• If you deactivate a picklist value from a custom field, it can still be used to set up a field filter.
Considerations for Setting Up Einstein Opportunity Scoring
Before setting up Einstein Opportunity Scoring, consider these requirements, limitations, and
EDITIONS
nuances.
Available in: Lightning
Note: Einstein Opportunity Scoring is available to users with a Sales Cloud Einstein license
Experience and Salesforce
and eligible customers without a Sales Cloud Einstein license.
Classic.
Available with Sales Cloud
Data Requirements and Access
Einstein, which is available
in Performance and
• You must have at least 200 closed won opportunities in last 24 months, each with a lifespan of
Unlimited Editions, and for
at least 2 days.
an extra cost in Enterprise
• You must have at least 200 closed lost opportunities in last 24 months, each with a lifespan of
Edition
at least 2 days.
Available to eligible
• Opportunity history shows an average of one update to each closed opportunity.
customers for no extra cost
• Use the standard opportunity Stage field because it’s used to calculate win rates, and win rates
in: Enterprise, Performance,
are used to generate scores. If you change the names of the opportunity stage picklist values,
and Unlimited Editions
make sure that the values are mapped to the correct stage type: Open, Closed/Won. or
Closed/Lost.
• If your win rate is extremely high or low, your scores could be skewed. For example, if your win rate is above 90 percent, you could
get a large number of opportunities with scores above 90. To avoid skewed scores, make sure that opportunities are set to the correct
closed stage. (A win rate is calculated by dividing the last two years of closed-won opportunities by all closed opportunities from
that same period.)
• If you don’t have enough opportunity data to build your own predictive model, Einstein uses a global model. The global model uses
anonymous data from many Salesforce customers. When you accumulate enough opportunity data, Einstein builds a scoring model
with your data and uses the model with the better results.
• After you turn on Einstein Opportunity Scoring, it can take up to 48 hours to analyze your data, build a scoring model, and add scores
to opportunities. You can check the status from the Einstein Opportunity Scoring setup page. If Einstein is still analyzing your data
after 48 hours, turn off Einstein Opportunity Scoring and then turn it on again, or edit your settings.
• Depending on when you purchased Sales Cloud Einstein, Einstein Opportunity Scoring might be on by default. If it is, scores aren’t
available for opportunities that are related to a person account. To get scores on those opportunities, turn off Einstein Opportunity
Scoring and then turn it on again.
• If you don’t have any Sales Cloud Einstein licenses but your org meets specific requirements, all users with a Salesforce user license
have access to scores on all opportunities. For information about your eligibility, contact Salesforce Customer Support.
10

Considerations for Setting Up Sales Cloud Einstein Considerations for Setting Up Einstein Forecasting
Reporting
• Opportunity scores are available in standard reporting and in custom report types. Model factors, which are used to build scoring
models, are available in custom report types. For examples, see Create Custom Report Types for Einstein Opportunity Scoring.
Field-Level Security
• For each opportunity score, Einstein shows the factors that have contributed most to the score. The contributing factors that sales
reps see alongside opportunity scores are dependent on the reps’ field access. For example, reps who don’t have access to the
Amount field don’t see factors that are based on amount. Keep in mind that factors include only field names, not field values. For
example, the Amount keeps going up factor doesn’t shows amount values to any users.
Lightning Experience and Salesforce Classic
• In Lightning Experience, we show Not Available when there’s no score. We show Hidden when a score isn’t available
because the user has limited access to opportunity scores. In Salesforce Classic , we show a blank value when there’s no score and
when a score isn’t available due to limited user access. For details on why there’s no score, see Understand How Einstein Scores Your
Opportunities.
• In Lightning Experience, when you use the Opportunity Score field in any type of filtering, use null in the filter criteria (when
non-numeric values are allowed) to include opportunities that Einstein hasn’t calculate a score for yet. Use -1 in the filter criteria
to include opportunities that don’t have scores because of limited access to opportunity scores. In Salesforce Classic, for the same
scenarios use null in the filter criteria (when non-numeric values are allowed).
Considerations for Setting Up Einstein Forecasting
Before setting up Einstein Forecasting, review the requirements and considerations.
EDITIONS
• Salesforce Forecasting must be enabled.
Available in: Lightning
• You must work with opportunities in Salesforce for at least 12 months. Specifically, the
Experience and Salesforce
opportunity history must show at least one update in each of the past 12 months.
Classic
• You must use a standard fiscal year. Standard fiscal years follow the Gregorian calendar, but
can start on the first day of any month of the year. Available with Sales Cloud
Einstein, which is available
• Forecasts must be measured by opportunity revenue. Predictions are generated for only the
in Performance and
oldest activated opportunity revenue forecast type.
Unlimited Editions, and for
• Your forecast hierarchy must include at least one forecasting enabled user who reports to a
an extra cost in Enterprise
forecast manager. Edition
• The Amount field should be populated in at least 80 percent of open opportunities.
• Opportunity splits aren’t supported. The forecast predictions are based on total revenue, not
shared revenue.
• You must use the standard Opportunity object and the standard Close Date and Amount fields. Custom date fields aren’t supported.
• To view the prediction graph on the home page when Einstein Forecasting is enabled, you must enable historical trending for
Forecasting Item.
• You can use Einstein Forecasting only in production orgs, not sandboxes.
• Avoid setting field-level security on the Sales Insights Integration User Profile for opportunity fields that you want to use to optimize
your predictions. It can impact your forecasting accuracy.
11

Considerations for Setting Up Sales Cloud Einstein Considerations for Setting Up Einstein Forecasting
• If you plan to use field filters to segment your opportunities, be aware of what happens when you delete or deactivate picklist field
values.
– If you delete a picklist value from a standard field, you can’t use the value to set up a field filter.
– If you deactivate a picklist value from a standard field, you can’t use it to set up a field filter. However, existing field filters based
on that value still work with opportunity records that contain the deactivated value.
– If you create a field filter using a standard field value and then delete the filtered value from the field, the filter still functions, but
appears in Setup with a blank value.
– If you delete a picklist value from a custom field, it still appears in Setup, but any filter created with that value doesn’t function.
– If you deactivate a picklist value from a custom field, it can still be used to set up a field filter.
12

SET UP SALES CLOUD EINSTEIN
Use the Sales Cloud Einstein Setup Assistant to get the targeted guidance you need for setting up
EDITIONS
the Sales Cloud Einstein features you want.
Available in: Lightning
Note: The following information is for Salesforce orgs with at least one Sales Cloud Einstein
Experience and Salesforce
add-on license. If you’re using Sales Cloud Einstein features with only Salesforce user licenses,
Classic
see Set Up Einstein Opportunity Scoring for Sales Cloud Users.
Available for an extra cost
in: Enterprise, Performance,
Select Who Can Use Sales Cloud Einstein
and Unlimited Editions
The Sales Cloud Einstein Included and Sales Cloud Included Bundle standard permission sets
include the permissions for Sales Cloud Einstein features. The permission sets also include some
CRM Analytics features, such as dashboards and the ability to analyze your report data using USER PERMISSIONS
Einstein Discovery for Reports. Assign a permission set to users.
To set up Sales Cloud
Access the Sales Cloud Einstein Setup Assistant
Einstein:
The Setup Assistant is your guide to selecting Sales Cloud Einstein users and setting up features. • Customize Application
AND Modify All Data
Enable Einstein Automated Contacts
Help reps spend even less time on data entry. Einstein Automated Contacts uses email and
event activity to find new contacts and opportunity contact roles to add to Salesforce. Choose
whether Einstein suggests the new data, which reps can add with just a couple of clicks, or adds it automatically.
Enable Einstein Lead Scoring
Give your sales team access to scores that help them prioritize leads. Turn on Einstein Lead Scoring, and then select a lead conversion
milestone to use, which leads to score, and which lead fields to consider during scoring.
Enable Einstein Opportunity Scoring
Give your sales team access to scores that help them focus on the right deals. When you set up Einstein Opportunity Scoring, you
choose whether to have Einstein consider all opportunity records and opportunity fields or only a subset. If Einstein Opportunity
Scoring is on by default, make sure that scores appear where you want, such as your customized opportunity page layouts and
public list views.
Enable Einstein Forecasting
Provide your forecast managers with AI-powered intelligence that improves forecasting accuracy, predicts results, and tracks how
sales teams are doing.
Troubleshoot Sales Cloud Einstein Setup Errors
When setting up Sales Cloud Einstein features, several important steps occur behind the scenes. If one of the steps isn’t successful,
one or more features can’t be enabled. There are several ways to troubleshoot setup issues.
13

Set Up Sales Cloud Einstein Select Who Can Use Sales Cloud Einstein
Select Who Can Use Sales Cloud Einstein
The Sales Cloud Einstein Included and Sales Cloud Included Bundle standard permission sets include
EDITIONS
the permissions for Sales Cloud Einstein features. The permission sets also include some CRM
Analytics features, such as dashboards and the ability to analyze your report data using Einstein
Available in: Lightning
Discovery for Reports. Assign a permission set to users.
Experience and Salesforce
1. From Setup, enter Permission Sets in the Quick Find. Then, select Permission Sets. Classic
2. Click the permission set you want to assign. Available with Sales Cloud
In Performance and Unlimited editions, assign the Sales Cloud Einstein Included or Sales Cloud Einstein, which is available
in Performance and
Included Bundle to users.
Unlimited Editions, and for
To access Sales Cloud Einstein using Performance or Unlimited editions, users must also have
an extra cost in Enterprise
the Salesforce standard user license. Edition
If you have users who accessed Sales Cloud Einstein through the Sales Cloud Einstein, Inbox,
Sales Engagement, or Revenue Intelligence license before Summer ’22, we recommend that
USER PERMISSIONS
you assign those users to the Sales Cloud Einstein Included or Sales Cloud Included permission
set, or a custom permission set that includes the Sales Cloud Einstein permission. To make these To create permission sets:
assignments, assign the new permission set to your users before removing the old permission • Manage Profiles and
set. Beginning in Summer ‘22, you can’t add users to the old Sales Cloud Einstein, Inbox, Sales Permission Sets
Engagement, or Revenue Intelligence permission sets. To assign permission sets:
In Enterprise Edition, assign the Sales Cloud Einstein permission set to users. • Assign Permission Sets
3. To assign the permission set to users, click Manage Assignments
Note:
• The standard Sales Cloud Einstein Included and Sales Cloud Included Bundle permission sets include the permissions for most
Sales Cloud Einstein features, plus access to dashboards. Account Insights and Opportunity Insights aren’t included with Sales
Cloud Einstein in Unlimited and Performance editions. Most permissions are enabled by default. To modify a permission set,
clone it and edit the app permissions.
• The standard Sales Cloud Einstein Included, Sales Cloud Einstein Included Bundle, and Sales Cloud Einstein permission sets
include the CRM Analytics permission Can Run Einstein Discovery for Reports. After Can Run Einstein Discovery for Reports is
assigned, you must enable CRM Analytics. Then users then get access to the Analyze button on reports, which lets users run
statistical analysis on their report data.
• The View Opportunity Scoring Model Factors permission, which lets users see the factors that are used to build opportunity
scoring models, isn’t enabled by default. Clone the Sales Cloud Einstein Included or Sales Cloud Included Bundle permission
set. Then, enable the View Opportunity Scoring Model Factors permission and assign the permission set to users. Users who
can view model factors can sometimes see the object data and object-related data used to build the models, regardless of
their sharing settings.
• The Sales Analytics app also comes with Sales Cloud Einstein but isn’t included in the Sales Cloud Einstein Included or Sales
Cloud Included Bundle permission set. You must set up permissions for the Sales Analytics App separately.
• If you used Sales Cloud Einstein before Spring ’18, you created a permission set with the Sales Cloud Einstein permission set
license. New permissions were added to the permission set license in later releases. Make sure the permissions for all the
Einstein features that you want to use, including analytics, are enabled in your permission set license.
14

Set Up Sales Cloud Einstein Access the Sales Cloud Einstein Setup Assistant
Access the Sales Cloud Einstein Setup Assistant
The Setup Assistant is your guide to selecting Sales Cloud Einstein users and setting up features.
EDITIONS
1. From Setup, enter Assisted Setup in the Quick Find box, then select Assisted Setup
under Einstein Sales. Available in: Lightning
Experience
Available with Sales Cloud
Einstein, which is available
in Performance and
Unlimited Editions, and for
an extra cost in Enterprise
Edition
USER PERMISSIONS
The setup page shows all the steps you need for Sales Cloud Einstein deployment, including
how to assign Einstein to users.
To access the Sales Cloud
Einstein Setup Assistant:
• Customize Application
AND Modify All Data
Enable Einstein Automated Contacts
Help reps spend even less time on data entry. Einstein Automated Contacts uses email and event
EDITIONS
activity to find new contacts and opportunity contact roles to add to Salesforce. Choose whether
Einstein suggests the new data, which reps can add with just a couple of clicks, or adds it
Available in: Lightning
automatically.
Experience
Important: Feature is scheduled for retirement on February 15, 2025. See Einstein Automated Available with Sales Cloud
Contacts Retirement. Einstein, which is available
1. From Setup, enter Assisted Setup in the Quick Find box, and then select Assisted Setup in Performance and
Unlimited Editions, and for
under Einstein Sales.
an extra cost in Enterprise
The Sales Cloud Einstein setup page shows all the steps you need for Sales Cloud Einstein
Edition
deployment, including how to assign Einstein to users.
2. Click Set Up next to Einstein Automated Contacts.
USER PERMISSIONS
3. On the Setup page, enable the types of data you want to suggest to users.
To enable Einstein
4. Select whether you want Einstein to automatically add new data or suggest it to users.
Automated Contacts:
Suggestions appear in the Einstein Insights component, so make sure that the Assistant
• Customize Application
component was added to the Home page and the Einstein Insights component was added to
AND Modify All Data
account and opportunity Lightning pages.
5. Make sure users have proper access to accounts, contacts, and opportunities.
To add or decline contact suggestions, users need edit access on accounts. To add or decline opportunity contact role suggestions,
users need edit access on opportunities, and read or edit access on contacts.
6. Make sure users have proper field-level security for the Lead Source field on contacts. The Lead Source field is used to create the
Added By Einstein list view.
15

Set Up Sales Cloud Einstein Enable Einstein Lead Scoring
7. To avoid errors when contacts are created, make sure that:
• All required contact fields have a default value.
• Einstein users have proper field-level security on all standard contact fields.
Enable Einstein Lead Scoring
Give your sales team access to scores that help them prioritize leads. Turn on Einstein Lead Scoring,
EDITIONS
and then select a lead conversion milestone to use, which leads to score, and which lead fields to
consider during scoring.
Available in: Lightning
Experience and Salesforce
Tip: Check out this feature in Sales Cloud Go! Find a guided setup experience, explore more
Classic.
content, discover related features, and monitor feature usage. See Discover and Set Up Sales
Cloud Features With Sales Cloud Go. Available with Sales Cloud
1. Go to Setup. In the Quick Find box, enter Einstein Lead Scoring, and select Einstein Einstein, which is available
for an extra cost in:
Lead Scoring under Einstein Sales.
Enterprise, Performance,
2. Turn on Einstein Lead Scoring.
and Unlimited Editions
3. Choose whether to use default settings or custom settings.
If you choose default settings, Einstein looks for leads converted to accounts and contacts, USER PERMISSIONS
scores all of your leads together, and considers all lead fields during scoring. When using default
settings, you can skip the remaining steps and click Score Leads. To enable Einstein Lead
Scoring:
4. If you chose custom settings, on the Conversion Milestone page, choose the lead conversion • Customize Application
milestone (accounts and contacts or opportunity creation) that matches your business practices.
AND
Does your sales team simply convert leads to accounts and contacts, or do they create
Modify All Data
opportunities when they convert leads? Then click Save & Next.
AND
5. On the Lead Segments page, choose whether you want Einstein to score all of your leads
View All Profiles
together, or only certain segments of your leads that meet criteria you specify. To score segments
of your leads separately, click Segments of Leads. Otherwise, click Save & Next.
Why would you want to score segments of your leads separately? Let’s say you have domestic leads and international leads. Their
conversion patterns could have significant differences. If you use the Country field to put them in different segments, Einstein can
calculate more accurate scores based on those patterns. Define your segments based on the criteria that make sense for your business.
6. If you want Einstein to score segments of your leads separately, click Add Segment.
a. Give the segment a name of up to 80 characters.
b. Choose whether to include records that meet all of your conditions or any of your conditions.
c. To add filter criteria for the segment, click Add Condition and then choose a field, operator, type and value.
You can specify up to 100 field filters for the leads you want to score. The CurrencyIsoCode field can’t be used in lead field filters.
The following field data types also can’t be used in lead field filters.
• Address
• Date
• Datetime
• Double
• Encrypted String
• Geolocation
16

Set Up Sales Cloud Einstein Enable Einstein Lead Scoring
• Multipicklist
• Reference — However, the RecordTypeId reference field is supported.
• Text Area
• Time
d. Add any other conditions you want the segment to meet.
e. Repeat the process for any additional lead segments you want to create. You can create up to 35 segments.
Leads that don’t meet the conditions for any segment are ignored when Einstein builds the predictive model.
f. If you created more than one lead segment, drag them into priority order. If a lead falls into multiple segments, Einstein scores
it as part of the highest priority segment.
g. When you’re done adding segments, click Save & Next.
7. On the Included Fields page, choose whether you want Einstein to include all your lead fields when building the predictive model
for each lead segment. By default, Einstein includes all lead fields. To include only certain fields, click Include Fields... and then
deselect the fields you don’t want Einstein to include. When you’re done, click Next.
Why would you tell Einstein not to include some fields? Some businesses use fields that don’t affect a lead’s chance of converting.
For example, you could have a field that indicates the reason a lead didn’t convert. Telling Einstein to exclude those fields yields
more accurate lead scores. Before excluding a field, make sure that the field doesn't affect the lead's chance of converting. Excluding
fields that do affect score analysis decreases the accuracy of your lead scores. If you’re uncertain about whether to exclude a particular
field, include it and then check the Einstein Lead Scoring dashboard to see what effect it has on your scores.
If you tell Einstein to score all leads together in the All Leads (Default) segment, Einstein includes any new fields you add to leads
automatically. If you create lead segments, add any new fields to your segments manually in Setup. If you decide to delete an included
field from the Lead object, exclude the field from all segments and wait for Einstein to update your scores before deleting it.
8. On the Review Settings page, confirm your choices. If you want, you can edit them.
9. When you’re done, click Score Leads.
Einstein analyzes your teams’ past converted leads to build a scoring model for each lead segment. It can take up to 48 hours to
analyze your data, build a scoring model for each lead segment, and add scores to leads. To check the status, return to the Einstein
Lead Scoring setup page.
When you score all leads together without creating segments, and you don’t have enough lead conversion data to build your own
predictive model, Einstein uses a global model. The global model uses anonymous data from many Salesforce customers. When
you accumulate enough lead data, Einstein builds a scoring model with your data and uses the model with the better results.
10.Using the Lightning App Builder, make sure that the Einstein Lead Scoring component was added to Lightning pages for leads. In
Salesforce Classic, add the Lead Score field to lead page layouts. The Lead Score field can’t be used on the same page layout as the
Lead Score Distribution or Conversion Rate by Lead Score report components.
To see the Einstein Lead Scoring component, users must have read access to the Company, Phone, and Email fields on leads.
11.After scores are available, add the Lead Score field to public lead list views. Salesforce automatically adds this field to default list
views.
Tip: To get the most out of Einstein Lead Scoring, tell sales reps to add the Lead Score field to their lead list views.
If you want to update your lead scoring setup, your changes become draft settings until you click Score Leads again. You can save your
draft settings and update them as often as necessary before using them to score leads.
17

Set Up Sales Cloud Einstein Enable Einstein Opportunity Scoring
If you choose to change your Einstein Lead Scoring settings, and CRM Analytics Data Sync is also enabled, you can see errors during data
sync. These errors occur because the ScoreIntelligenceId field on leads is unavailable for data sync while Einstein rebuilds your lead
scoring model. The data sync errors resolve when the model is rebuilt, and updated scores appear on lead records.
If you previously turned off Einstein Lead Scoring and are turning it back on, update settings in the Einstein Lead Scoring app in Analytics
Studio.
• In Analytics Studio, click the Einstein Lead Scoring app.
• Click Reconfigure app. If you don’t see that link, click New version available.
• Read the message about overwriting existing customizations, and then select It’s OK to overwrite current app and any
customizations.
• Click Continue.
Enable Einstein Opportunity Scoring
Give your sales team access to scores that help them focus on the right deals. When you set up
EDITIONS
Einstein Opportunity Scoring, you choose whether to have Einstein consider all opportunity records
and opportunity fields or only a subset. If Einstein Opportunity Scoring is on by default, make sure
Available in: Lightning
that scores appear where you want, such as your customized opportunity page layouts and public
Experience and Salesforce
list views.
Classic.
Note: If you use Sales Cloud Einstein features without any Sales Cloud Einstein add-on Available with Sales Cloud
licenses, and it’s your first time setting up Einstein Opportunity Scoring, see Set Up Einstein Einstein, which is available
Opportunity Scoring for Sales Cloud Users. in Performance and
Unlimited Editions, and for
Tip: Check out this feature in Sales Cloud Go! Find a guided setup experience, explore more
an extra cost in Enterprise
content, discover related features, and monitor feature usage. See Discover and Set Up Sales
Edition
Cloud Features With Sales Cloud Go.
Available to eligible
1. To open the Einstein Opportunity Scoring setup page, do one of the following.
customers for no extra cost
• In Lightning Experience, from Setup, enter Assisted Setup in the Quick Find box, in: Enterprise, Performance,
and then select Assisted Setup. Then, click Set Up next to Einstein Opportunity Scoring. and Unlimited Editions
• In Salesforce Classic, from Setup, enter Einstein Opportunity Scoring in the
Quick Find box, and then select Einstein Opportunity Scoring. USER PERMISSIONS
2. Read the introduction, and then click Next. To set up Einstein
Opportunity Scoring:
3. Choose whether to have Einstein consider all opportunity records or only a subset when building
• Customize Application
the scoring model. Then, click Next. If needed, define the conditions, and click Next.
AND Modify All Data
When you give Einstein only a subset of opportunities to look at, it can yield more accurate
AND View All Profiles
scores. For example, if you use external systems to create opportunities that are closed rather
quickly, those opportunities don’t reflect the normal opportunity lifecycle and can skew your
scores.
When defining conditions, you can use up to 100 fields. The CurrencyIsoCode field isn’t available. The following field data types
aren’t supported.
• Address
• Date
• Datetime
• Double
18

Set Up Sales Cloud Einstein Enable Einstein Opportunity Scoring
• Encrypted String
• Geolocation
• Multipicklist
• Reference (However, the RecordTypeId reference field is supported.)
• Text Area
• Text Area
• Time
4. Choose whether to have Einstein consider all opportunity custom fields when building the scoring model. Then, click Next. If needed,
deselect the fields you want Einstein to exclude, and click Next.
Exclude fields from the model only if you’re sure they aren’t part of the opportunity lifecycle. For example, you can safely exclude
automatically generated fields, such as IDs and dates. Mistakenly excluding influential fields makes opportunity scores less accurate.
If you’re unsure about whether to exclude a certain field, err on the side of caution and include the field.
5. Review your settings. Then, click Start to begin the scoring process.
It can take up to 48 hours to analyze your data, build a scoring model, and add scores to opportunities. To check the status, return
to the Einstein Opportunity Scoring setup page. If you don’t have enough opportunity data to build your own predictive model,
Einstein uses a global model. The global model uses anonymous data from many Salesforce customers. When you accumulate
enough opportunity data, Einstein builds a scoring model with your data and uses the model with the better results.
6. Make sure that the Opportunity Score field is on your opportunity page layouts.
• In Lightning Experience (Grouped view), add the Opportunity Score field to your customized opportunity page layouts. Salesforce
automatically adds this field to default compact layouts.
• In Lightning Experience (Full view), Salesforce automatically adds the Opportunity Score field to the Details section of your default
and custom layouts.
• In Salesforce Classic, add the Opportunity Score field to your customized page layouts for opportunities. Salesforce automatically
adds this field to the Details section of default page layouts.
7. By default, the Opportunity Score field is on the Recently Viewed list view for opportunities, but add it to public opportunity list
views. To get the most out of Einstein Opportunity Scoring, ask your sales teams to add this field to their own opportunity list views.
8. If you use forecasts, add the Opportunity Score field to the opportunity list on the forecasts page.
9. Add the Opportunity Score field to your opportunity reports where appropriate.
19

Set Up Sales Cloud Einstein Enable Einstein Forecasting
Enable Einstein Forecasting
Provide your forecast managers with AI-powered intelligence that improves forecasting accuracy,
EDITIONS
predicts results, and tracks how sales teams are doing.
Available in: Lightning
Tip: Check out this feature in Sales Cloud Go! Find a guided setup experience, explore more
Experience and Salesforce
content, discover related features, and monitor feature usage. See Discover and Set Up Sales
Classic
Cloud Features With Sales Cloud Go.
Available with Sales Cloud
Important: To enable users for Einstein Forecasting, make sure they’re enabled to use
Einstein, which is available
forecasts and are assigned as a forecast manager.
in Performance and
1. From Setup, enter Assisted Setup in the Quick Find box, and then select Assisted Setup. Unlimited Editions, and for
The setup page shows all the steps you need for Sales Cloud Einstein deployment, including an extra cost in Enterprise
how to assign users. Edition
2. Click Set Up next to Einstein Forecasting.
USER PERMISSIONS
3. Click Enable.
4. Read the introduction, and then click Next. To enable Einstein
Forecasting:
5. Choose whether to have Einstein consider all opportunity records or only a subset when building
• Customize Application
the predictive model. Then, click Next. If needed, define the criteria, and click Next.
AND Modify All Data
6. Choose whether to have Einstein consider all custom opportunity fields when building the
predictive model. Then, click Next. If needed, deselect the fields you want Einstein to ignore,
and click Next.
7. Review your settings. Then, click Save.
8. If you customized the Home page, add the performance chart to it.
Note: Einstein uses your data to create your custom predictive model. If organization-wide sharing is set to Private for the User
object, to extract relevant information, you might need to give a couple profiles access to users. Make sure the Analytics Cloud
Security User and Analytics Cloud Integration User profiles have the View All Users system permission.
Troubleshoot Sales Cloud Einstein Setup Errors
When setting up Sales Cloud Einstein features, several important steps occur behind the scenes. If
EDITIONS
one of the steps isn’t successful, one or more features can’t be enabled. There are several ways to
troubleshoot setup issues.
Available in: Lightning
If you still have issues after following the troubleshooting steps, contact Salesforce Customer Support. Experience and Salesforce
Classic.
Verify the Integration User Profile Details Available with Sales Cloud
Einstein, which is available
Sales Cloud Einstein creates an integration user and assigns it an integration user profile. We updated for an extra cost in:
the names of the integration user, profile, and connected app. If you purchased Sales Cloud Einstein Enterprise, Performance,
before April 15, 2019, the old and updated names are listed in your org. When troubleshooting and Unlimited Editions
setup issues, refer only to the updated names and IP addresses.
Integration User Name Integration User Profile Name Connected App
Sales Insights Integration Sales Insights Integration User OIQ_Integration
20

Set Up Sales Cloud Einstein Troubleshoot Sales Cloud Einstein Setup Errors
Supported IP Addresses
35.155.249.183 44.225.239.10
35.160.107.125 44.225.27.211
35.163.185.97 44.226.10.160
35.163.211.82 44.226.28.151
35.163.248.132 44.226.81.25
35.164.15.153 52.26.247.68
35.164.61.92 52.40.129.165
35.165.218.130 52.40.253.214
44.224.239.117 54.148.110.202
44.224.5.68 54.200.204.60
44.225.115.174 54.214.184.254
44.225.191.69 54.69.64.221
100.21.158.232 100.21.112.198
Confirm that the integration user profile:
• Is assigned to the integration user.
• Has read access to the relevant objects and fields. For example, for Einstein Lead Scoring to determine which fields are important
to your lead conversion patterns, the integration profile needs access to all lead fields.
• Has a supported login IP addresses assigned. See table.
• Has access to the connected app. Here’s how to check access.
1. From Setup, enter Profiles in the Quick Find box, and then select Profiles.
2. Click the Sales Insights Integration User profile.
3. From the Connected App Access section, confirm that the profile has access to the OIQ_Integration connected app.
Verify the Connected App Details
Sales Cloud Einstein features use a connected app to create a secure connection between Salesforce data and our sales intelligence
infrastructure.
• Confirm that the app is installed.
1. From Setup, enter Installed Packages in the Quick Find box.
2. Confirm that the Sales Insights package is listed under Installed Packages.
3. If you don’t see the package in the list, download it from the Salesforce App Installation page.
• Confirm that the connected app has the correct OAuth policy and user profile assigned.
1. From Setup, enter Connected Apps in the Quick Find box, and then click Manage Connected Apps.
2. Click the OIQ_Integration app.
3. From the OAuth Policies section, confirm that the Permitted Users field is set to Admin approved users are pre-authorized.
21

Set Up Sales Cloud Einstein Troubleshoot Sales Cloud Einstein Setup Errors
4. From the Profiles related list, confirm that the Sales Insights Integration User profile is assigned.
22
