# Relax Data Science Challenge
The data is available as two attached CSV files:   
*takehome_user_engagement.csv*  
*takehome_users.csv*

The data has the following two tables:   
1] A user table (*"takehome_users"*) with data on 12,000 users who signed up for the product in the last two years.  This table includes:   

● __name__: the user's name   
● __object_id__: the user's id   
● __email__: email address   
● __creation_source__: how their account was created. This takes on one of 5 values:   
○ __PERSONAL_PROJECTS__: invited to join another user's personal workspace   
○ __GUEST_INVITE__: invited to an organization as a guest (limited permissions)   
○ __ORG_INVITE__: invited to an organization (as a full member)   
○ __SIGNUP__: signed up via the website   
○ __SIGNUP_GOOGLE_AUTH__: signed up using Google Authentication (using a Google email account for their login id)   
● __creation_time__: when they created their account   
● __last_session_creation_time__: unix timestamp of last login   
● __opted_in_to_mailing_list__: whether they have opted into receiving marketing emails   
● __enabled_for_marketing_drip__: whether they are on the regular marketing email drip   
● __org_id__: the organization (group of users) they belong to   
● __invited_by_user_id__: which user invited them to join (if applicable).   

2] A usage summary table (*"takehome_user_engagement"*) that has a row for each day that a user logged into the product. 

Defining an "adopted user" as a user who has logged into the product on three separate days in at least one seven-day period, **identify which factors predict future user adoption.** 
 
We suggest spending 1-2 hours on this, but you're welcome to spend more or less. Please send us a brief writeup of your findings (the more concise, the better -- no more than one page), along with any summary tables, graphs, code, or queries that can help us understand your approach. Please note any factors you considered or investigation you did, even if they did not pan out. Feel free to identify any further research or data you think would be valuable. 

# Conclusion
The most important 3 factors predict future user adoption are:
1. **org_id**: the organization (group of users) they belong to
2. **invited_by_user_id**: which user invited them to join (if applicable)
3. **opted_in_to_mailing_list**: whether they have opted into receiving marketing emails

Also, **creation_source_PERSONAL_PROJECTS** (invited to join another user's personal workspace) and **enabled_for_marketing_drip** (whether they are on the regular marketing email drip) are important as well. 

For creation source, the order of importance are:
1. __PERSONAL_PROJECTS__: invited to join another user's personal workspace
2. __ORG_INVITE__: invited to an organization (as a full member) 
3. __GUEST_INVITE__: invited to an organization as a guest (limited permissions)
4. __SIGNUP_GOOGLE_AUTH__: signed up using Google Authentication (using a Google email account for their login id) 
5. __SIGNUP__: signed up via the website
