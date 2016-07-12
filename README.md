# Nerfbort Research

Sperglord Nerboard is a Facebook group with small (~110) commnity compoased
of several groups of people who know each other from different purposes, 
relationships, communities, timelines, cities and states.

`fb-snfl-awks` stands for *Facebook-Sperglord Nerbort-alpha* application. This
project may be re-named to `fb-group-modsrgods` for *Facebook Group
Moderation-on-Demand System: "Responding to Guilt and Death Successfully"*

## Sperglord Nerfbort Facebook research applications.

Reducing audience attrition, "shitposting," "copypasta," and becoming a
"funeral home for dead memes," and improving community growth, engagement,
and ratio of quality posts is important. 

Moderation is hard. Can moderation be automated, while respecting the taste
of the community? Can presentation of content affect and improve growth and
engagement by hiding content from certain users, and encourage activity in
segmented sub-commnuties? 

---

## Keeping a community engaged and contributing quality content.

Running a Facebook group can be diffcult, even when it's small. Growing a
community and keeping an audience engaged and encouraged to actively
interact, comments, and post is the ideal outcome. However, moderation is
necessary to keeping an audience engaged: a small sample of irritating
users, posts, or comments may irritate an audience and cause exodus. Though
daily activity is an ongoing goal, the risk of low signal-to-noise, or
contribution by a few, or questionable content could reduce an audience's
attention.

This project aims to investigate two methods to improve content quality and
encourage user engagement.

### 1. Automated moderation

To ensure a high quality of content, moderation has been deemed invaluable.
With that being said, moderation is a inperfect science that requires trust
from moderators, and can still be wrought with bias and a poor reaction from
the community: ideally, the community is educated on what content is acceptable,
and not punished for posting discouraged content. Ideally moderation controls
the content, but also explains to a user why the content was removed. Secondly,
moderation should be consistent. 

#### Proposal

Attempt to automate moderation.

*  Establish a guideline for content.
*  Rule-based heuristics for content.
*  Record how existing moderators responded to content.
*  Evalatuate and build Bayesian parameters from moderated content.
*  Create 5-20 groups of Bayesian parameter rulesets.
*  Identify the inappropriateness of content, by group.
*  Identity metrics to auto-moderate by: 
   -  # of high-valued probability in a number of groups,
   -  extremely high-valued probability in a singular group,
   -  etc.
*  Run that shit, record moderated content.
*  Identify metrics to measure audience response:
   -  # of posts less per day and per week, after moderation
      -  ...is moderation too strong?
      -  ...is moderation impacting the community negatively?
      -  ...is moderation dropping suddenly?
      -  ...should auto-moderation be slowed down, decreased, or removed?
   -  % of interactivity per post and/or comment per day and per week
      -  has attrition been attenuated -- needs weeks of study.
*  Adjust moderation parameters, aggressiveness, probability thresholds,
   consistency, etc.
*  Consider different strategies to adjust moderation.
*  Apply A/B tests using sets of adjusted moderation strategies.
*  Automate the creation of strategies, and consider the performance 
   of already-attempted strategies.
*  Re-evaluate (i). Find inspiration.
*  Automate (i) similar to (j) to find parameter sets that show positive
   trends and parameter sets that show negative trends, and apply the
   functionality used in (k) through (m) to determine parameter sets that
   show significant change over A & B, over time, or high variability.
*  Chill out. You've automated moderation.
  
#### Highdeas

*  Read Facebook public feed
*  Collect data per post:
   -  Poster
      -  Type: Group, Page, Person
      -  Affilitiations:  News outlet, etc.
   -  Privacy:  Public, group-only, etc.
   -  Type: Image, Video, etc.
*  Check against database of content
*  Provide metrics
   -  Frequency of (Post Type)
   -  Every (Hour, Day, Week)
   -  Where (Public feed, Group feed, etc)

### 2. Bulletin Board System (BBS)

Acknowledge and encourage micro-communities without hassle.

A popular strategy with multiple large and closed Facebook communities is
to splinter into more Facebook groups, in order to capture the signal-to-
noise ratio for a topic and locazize it to a dedicated Facebook group while
maintaining the diversity of the original group and community.

Stupid and inefficient. Facebook groups are too ephermal, it's difficult to
keep a post (or a thread) going, because a large community that creates a 
lot of content is going bury subsequent content. This is similar to the 
community content and interaction seen on large 4chan boards; while this
encourages valued threads to remain visible on the first page, it's an unfair
comparison: in a Facebook group, it's not as easy to return to older content,
which may lead to inhibited engagement and contribution. Secondly a Facebook
group does not have micro-discussion boards dedicated to an interest or
topic.

#### Proposal

This is a pipe-dream to return to the old days of Bulletin Board Systems,
simialr to communities powered by vBulletin, phpBB, YABB, etc.

*  Ideally, posts will be grouped by similarity and grouped into a single thread.
*  If discussion is related to the original post and content, but significantly
   different, or a long time has passed, create a new thread (i.e., prevent
   off-topic behavior in a thread; prevent ressurecting dead threads).
*  Similarly, move a significant comment thread to its own thread if it's become
   relatively active and/or is significantly different from the original post.
*  If enough discussion threads are created for the same topic, attempt and/or
   consider grouping these threads and moving to its own sub-forum.
   -   Many posts are images, and may not include threads. How should these posts
       be grouped? 
   -   Possible solution:  
       -   Google image reverse search for the image
       -   Save returned images, ranked by page in search results (linearly or
           logarithmically), and ranked by related-image within a primary hit.
       -   Save all returned images, reduce images to short byte strings to easily
           determine similarity distance between images.
       -   Determine threshold parameters to determine if is similar to a result
           set is similar or falls within the scope of a previous performed search:
           -   # of hits to existing database, averaged by ranks, or other method
           -   # similarity of hits of related images
       -   Group image posts to appropriate topic to determine the thread or sub-
           forums they belong in.
*  So much mindblowingly tedious small things.

#### Questions

*   Standalone application and separate website powered by Facebook Connect?
*   Integrated as a native Facebook application. Is this possible? Is this 
    useful? Will this cause confusion, splinter a community?
*   Will it result into splintered but encourage micro-communities?
*   How to discourage use of Facebook group and encourage use of app?
*   How much data to store locally? Should content be powered by Facebook, or
    scrubbed and kept locally? (i.e., to keep Facebook group scrubbed to
    redirect community and encourage engagement using the app.)
*   Opening the platform to support multiple Facebook groups, shown as multiple
    forums, or the user creates rulesets to create and show threads:
    -   By group: Powered by a user-defined whitelist/blacklist of groups,
        or topics, or determine which deserve to be primary forums.
    -   Grouping groups: create forums by combinining content generated in 
        several groups, powered by a user-defined whitelist/blacklist
        of groups or topoic list.
    -   Repeat (i) - (ii) to segment groups or content into seperate sub-forums.

#### Potential issues

*  Permission and user credentails.
   -  Moving posts to different threads and subforums.
   -  Interacting Facebook CMS API to determine the approprate group, post, and
      comment thread to add/edit/move/split/slice/delete content, despite data 
      is organized by BBS schema of forum/sub-forum/thread/post/reply, very 
      different from Facebook's group discussion schema.

#### TL;DR

Sounds hard. May attempt to implement a read-only solution.
  
## System architecture proposal

### Procedures and pipeline

1.  Stand up Heroko application. (easy deployment and CI/CD pipeline)
2.  Record content parameters in document storage.
3.  Record determined content parameters and bayesian rulesets in RDBMS.
4.  Record moderation actions and auto-moderation and A/B results in RDBMS.
5.  Record determined forum/sub-forum/thread/post/reply relationships in RDBMS.
6.  Stand up ELK stack to record metrics and create dashboards to analyze.
7.  Create read-only demonstration, evaluate.

### Implementation details

1.  Python application; explore Scala application
2.  MySQL RDBMS; Mongo long-term content storage; ElasticSearch query-optimized
    storage; Logstash for importing/exporting datasets; Kibana to create dashboards
    and evaluation
3.  Start on standalone application; eventually see if Facebook Canvas is 
    possible and determine to attempt.
        
## Specified guidelines

## Prior art

[Keyword-based automatic moderation](https://www.agorapulse.com/features/facebook-automatic-moderation-tools).
