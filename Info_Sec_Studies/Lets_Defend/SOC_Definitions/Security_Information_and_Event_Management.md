A SIEM is a security solution that provides the real time logging of events in an environment. The actual purpose for event logging is to detect security threats.
\
In general, SIEM products have a number of features. The ones that interest us most as SOC analysts are: they filter the data that they collect and create alerts for any suspicious events.
\
Example of an alert: If someone on a Windows operating system attempts to enter 20 incorrect passwords in 10 seconds, this is suspicious activity, it is not likely that someone who forgot their password would try to re-enter their password so many times in such a short period. This is why we create a SIEM rule/filter, to determine such activates that exceed the threshold values. Due to this SIEM rule an alert will be created if such a situation occurs.
\
Some popular SIEM solutions are:
- [[IBM_QRadar]]
- [[ArcSight_ESM]]
- [[FortiSIEM]]
- [[Splunk]]
