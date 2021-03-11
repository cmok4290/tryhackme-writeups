# Splunk

## [Task 1] Deploy!

## [Task 2] Can you dig it?
1. Splunk queries always begin with this command implicitly unless otherwise specified. What command is this? When performing additional queries to refine received data this command must be added at the start. This is a prime example of a slight trick question.
    - search
2. When searching for values, it's fairly typical within security to look for uncommon events. What command can we include within our search to find these?
    - rare
3. What about the inverse? What if we want the most common security event?
    - top
4. When we import data into splunk, what is it stored under?
    - index
5. We can create 'views' that allow us to consistently pull up the same search over and over again; what are these called?
    - dashboard
6. Importing data doesn't always go as planned and we can sometimes end up with multiple copies of the same data, what command do we include in our search to remove these copies?
    - dedup
7. Splunk can be used for more than just a SIEM and it's commonly used in marketing to track things such as how long a shopping trip on a website lasts from start to finish. What command can we include in our search to track how long these event pairs take?
    - transaction
8. In a manner similar to Linux, we can 'pipe' search results into further commands, what character do we use for this
    - |
9. In performing data analytics with Splunk (ironically what the tool is at it's core) it's useful to track occurrences of events over time, what command do we include to plot this?
    - timechart
10. What about if we want to gather general statistical information about a search?
    - stats
11. Data imported into Splunk is categorized into columns called what?
    - fields
12. When we import data into Splunk we can view it's point of origination, what is this called? I'm looking for the machine aspect of this here.
    - host
13. When we import data into Splunk we can view its point of origination from within a system, what is this called?
    - source
14. We can classify these points of origination and group them all together, viewing them as their specific type. What is this called? Use the syntax found within the search query rather than the proper name for this.
    - sourcetype
15. When performing functions on data we are searching through we use a specific command prior to the evaluation itself, what is this command?
    - eval
16. Love it or hate it regular expression is a massive component to Splunk, what command do we use to specific regex within a search?
    - rex
17. It's fairly common to create subsets and specific views for less technical Splunk users, what are these called?
    - pivot table
18. What is the proper name of the time date field in Splunk?
    - \_time
19. How do I specifically include only the first few values found within my search?
    - head
20. More useful than you would otherwise imagine, how do I flip the order that results are returned in?
    - reverse
21. When viewing search results, it's often useful to rename fields using user-provided tables of values. What command do we include within a search to do this?
    - lookup 
22. We can collect events into specific time frames to be used in further processing. What command do we include within a search to do just that?
    - bucket
23. We can also define data into specific sections of time to be used within chart commands, what command do we use to set these lengths of time? This is different from the previous question as we are no longer collecting for further processing.
    - span
24. When producing statistics regarding a search it's common to number the occurrences of an event, what command do we include to do this?
    - count
25. Last but not least, what is the website where you can find the Splunk apps at?
    - splunkbase.splunk.com
26. We can also add new features into Splunk, what are these called?
    - apps
27. What does SOC stand for?
    - Security Operations Center
28. What does SIEM stand for?
    - Security Information and Event Management
29. How about BOTS?
    - Boss of the SOC
30. And CIM?
    - Common Information Model
31. What is the website where you can find the Splunk forums at?
    - answers.splunk.com


