What is a [[SIEM]]
\
Well how about the relationship between a SOC Analyst and a SIEM:
\
Although [[SIEM]] solutions have many features, as SOC analysts we generally only follow alerts. There are other groups/people who develop configurations and rule correlations.
\
Alerts are create by data that is passed through filters. The alerts are primarily analyzed by a SOC analyst. This is exactly where a SOC analyst's duty in the SOC begins. Fundamentally, you must decide whether this created alert is a real threat or a false alarm.
\
**An example of a false alarm:**

Let’s assume that a [[SIEM]] team put together a rule set that created alerts for URL addresses that had the word “union” in them and tried to detect SQL Injections.  
A user did a search using “https://www.google.com/search?q=sql+union+usage”, an alert was created in the [[SIEM]], it looks like there is no apparent danger. The alert was created because the keyword “union” was present in the URL. These kinds of exceptional situations can be communicated to the [[SIEM]] team to improve the alerting process.
