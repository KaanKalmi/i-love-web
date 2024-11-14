# The web performance landscape in 2024 - Tammy Everts
Key note of the first day sort of, linkedin.com/in/Tammyeverts

She wrote the book time is money, the business value of web performance, she also curates WPO stats
- [web prformance guide](speedcurve.com/web-performance-guide)
- Dunning-Kruger effect: cognitive bias in which people with limited competence in a particular domain **overestimate** their abilities, and people that are high performing tend to **underestimate** their abilities.

In other words we don't know what we don't know!

### Users: 
- There are 5.53 billion internet users
- 71.1% of internet users use android devices, but that leaps when you look at countries like india where there are 95% android users.
- Most countries are android dominant, 
- iPhone = iNequiality, inequiality is growing faster than the people in the bottom event can afford?
- LCP and INP on android became better for android users in 2 years (2022 - 2024)
- a significant chunk of the world has less than 50 megabits a second!

We have so many metrics, at speedcurve there are countless metrics like 50+ synthetic ones, 25 for every third party etc.

Google came up with a solution, which was just have 3 metrics : LCP, CLS. INP. They basically set aside the anxiety and frustration when looking at web performance metrics.

However none of these metrics have 100% browser adoption, as none of them have safari adaptation.
- 66% of the internet users uses chrome 
- 18% of the internet usets uses safari
Looking at these 2 stats, you can see that there is still a huge chunk missing with google's metrics.

- There is no consistent correlation with google's treshholds for 'good', 'needs improvement' and 'poor'.

### RECAP:
- We mostly build for iOS
- We mostly monitor performance in google
- Pages are becoming bigger in size
    - The amount of video and javascript sizes have exploded in 2 years time (median amount)
    - The amount of resource size is still exploding in vdeo's and JS files (90th percentile)
- We're still making the same optimization mistakes
- 19 of the 20 pages had an inefficient cache policy
- 17 of the 20 pages had unused js
- 16 out of 20 didn't enable bfcache registration
- 14 out of 20 have no width or height on their images
- only 2 out of 20 lazy loaded LCP images
- Performance and Accessibility should overlap, but currently they're not overlapping
- 96.3% of pages had WCAG failures

### Why are we making these mistakes?
- Maybe none of these issues affected the critical rendering path
- Maybe the optimization were hard to implement
- Maybe just didn't know

> Ask yourself this: who am i building for, testing for, are my pages getting faster, am i doing the right optimizations and does it help my business?

> As world best performance mom, she did not leave us on a high note...

# Site-Speed that sticks - Harry Roberts
> He's talking about monkeys and bananas, is he calling us monkeys! (just kidding)
> [His LinkedIn](https://www.linkedin.com/in/csswizardry/)

Not all successfull project, stay successfull. It's usually because of a lack of confidence and such.

### 5 key topics
1. Metrics
    - Not all metrics are born equal, certain metrics can only be used for certain parties.
    - Different metrics for different people, on different occasians, with different levels of disclosure.
    - The three key classifications for metrics are: KPIs Enablers and Predictors
        - KPIs: What are we working on? The metric used to measure success. A combination of definition and target!
        - Enablers: Metrics that directly influence KPIs but are not KPIs. A 500ms faster time in enablers, is not a 500ms faster time on KPIs.
        - Predictors: A strange metric, signals for good/bad performance, take it with a pinch of salt tho. Good for root causing and reverse engineering. It's also highly quantative. 

2. Localhost
    - The most depressing bit for a developer, Seldom live-like, pretty dang fast, un-bundled.
    - Know your tools, like google performance tab, shows you the 70th percentile performance of your pages.
    - Experiment with custom throttles, like 3G, LTE etc. So you get closer to a realistic user experience.
    - [coupon on csswizard](csswzz.it/perfnow25)
    - Slow down your backend, for local hosts
    - If you know you got 800ms render blocking time, force it by delaying it with [slowfiles](https://slowfil.es/)!
    - Core web vitals are too big for local host
    - If you're working locally, measure locally!
    - You can test something 5 times, take the third result (ascending order) and thats your median for the result!

3. Backstops
    - Backstop is a specific type of test that informs you if you might fail with a release
    - A budget is the question: What is the worst possible performane we will accept?
    - Set the boundary to your worst release!
    - Don't move your red line down, keep it at the highest, otherwise you basically didn't succeed in your sprint.
    - This is where synthetic testing comes into it
    - Synthethic testing; real user monitoring
    - Use predictors as tripwires
    - Budgets versus Targets; budgets are your backstops, your targets are your ambitions!
    
4. Monitoring
    - the **M** in RUM stands for monitoring.
    - Don't use synthethic testing for monitoring!
    - If you run a synthetic test every day, you run a difference in TESTING (Like speedcurve updating their testing tool).
    - Again, you're monitoring variation in tests
    - Only alert on your KPIs
    - Every 100ms you lose in the backend, you lose 100ms in the frontend!
    - Only fire alerts, or revert releases on your KPIs!
    - Always follow numbers

5. Playbook
    - Response = function(severity, duration)
    - Temporary severity is something like a big slowdown for just a day or 2 etc.
    - KPI regression of over 10% for one week for one week requires remedation in the next sprint. (Only if you talked about whats acceptible)
    - an enabler regression over any % needs the attention anytime in the current sprint
    - a predicter regression over any % needs attention in the next sprint

Early triage: Who, What, When, Where, Why?
- What regressed?
- When did it regress, is it still like that?
- Where did it regress?
- Who owns the problem? (not to point fingers, but to find who can assist)
- Why did it regress?

The `<head>` tag is the biggest render blocking element in HTML

### Key takeaways
- Increase confidence
- Use the right tool for the job
- Have a plan of attack
- Agree; Commit

> Q: At what point do you ditch the synthetic testing part? A: Start with RUM, work back from there. Your synthetic tests should still be reliable. I (Harry) would only use it as a response to atomic change, thus only use it as a response to a change you can pinpoint to (commits).

> Q: What about variations that happen in RUM data? A: Generally just segment things, if you see a random spike in dataa and you can see something got implemented there, change that. (not actually his answer i just forgot to note it down so now i got my own interpretation).

> Q: Do you have a recommendation on what metric to lower for companies? A: IT depends on their business motives, if it's e-commerce definetly get the LCP down on the important pages. 

# Accessible is performant- Eric Bailey
Performance: the manner in whih a mechanism behaves

How do you describe an interface?
- The accessibility tree: Running collection of objects that make up the UI. 
    - Without this functioning you don't know what the interface is!
    - How to build an accessibility tee:
        - Name
        - Role
        - Properties
        - Description
Putting these together gives you an object, like a play button. 

### How do you build these UI components?
- OS alert dialog
    - Menubar
        - Title
        - Close button
    - body
        - Title
        - Text
        - Save button
        - Cancel button

On the web: you render HTML, with it's appearance nad behavior augmented by CSS and JS. This makes the DOM tree, which browsers then read the DOM from and rendered AND THAT is what the user sees.

Running in parallel is the Accessibility tree, This makes a sampled version of the DOM which then gets read by the screenreaders.

The accessibility trees relies on the user being able to see and interact with the DOM tree.

It's more of a accessibility forest than a tree, because there are multiple trees. Different companies update and create new technologies for it.

The DOM can be a part of the accessibility tree, but it's more brittle than it.

### How do we prevent these problems?
- Write semantic HTML

### Let's make the abstract immediate
Material Design has trash HTML semantics, and overly long JS.

An optimal DOM tree has less than 1500 nodes max depth of 32 nodes and something else, this dude talks faster than eminem during his fastest verses....

A11Y is made specifically for accessibility and performance (they go hand in hand), as they had much, much less code than Material Design

This guy flamed Facebook on their dogshit trash code damn.

Screen readers: JAWS, NVDA, VoiceOver, Talkback

### How to test
- Start/Stop voice over
- Navigate by interactive item
- Did voice over crash? no? good, if it does simplify your experience (Clean your code and use semantics)

Performance: Ability to perform

Refer to WCAG 2.2 Understanding Docs. (I lost track)

> Q: What happens to the accessibility tree if the DOM gets loaded slower? A: It depends on the OS, device, browser etc. Most of the time it won't announce anything it will just create a buffer. So the response gets bufferd. 

# Performance mistakes - Paul Calvano
> This is one of the important talks for me as a student (stuff i can implement in my code), added later: Why this guy constantly out of breath tho... 
All of the data in this talk is from [HTTPArchive](httparchive.org)

### The 17 common mistakes
1. Not adding Lazy loading on LCP images
    - Won't load the images if it isn't on the viewport
    - [MDN Lazy loading](https://developer.mozilla.org/en-US/docs/Web/Performance/Lazy_loading)
    - Slows down Largest Contentful Paint
    - Lighthouse tells you when the LCP is lazy loaded
    - 4% of the sites in the HTTP Archive failed the audit 
    - Don't lazy load with fetch prioirty on high, that's like saying oh hey, don't load this but when you do load it fast!
2. Lazy loading high priority images
3. Async decoding on high priority images
4. preconnecting needs to have crossorigin attribute as well.
    - Out of the 9M preconnects, 4.6M missed a crossorigin attribute!
5. Preloading 
    - After preloading too much, preloading will delay other high priority resources!
    - 2.4M sites are using preloading, and around 140K are preloading multiple images, 48K are preloading more than 1MB of data, 34K preloading more than 20 requests and 1.2K preloading video's
6. Preloading excessive bytes
7. Don't preload video's
8. Unused preloads
    - This makes the browser preload unused data, which slows down your website.
    - Almost half the sites are using preload with unused data
9. You have to use the `as` attribute when preloading
    - Don't preload different variations of your font!
    - 37K websites are missing preload type
10. Preloading different variations of the same font 
11. Don't preload and swap display on your fonts
    - Only use 1 of the 2!
12. not content-encoding big content (No gzip or brotli compression)
    - Content-encoding just compresses your content
    - Brotli is a good compression tool, but gzip is supported by every broswer as of 2024.
    - [His compression testing tool](https://tools.paulcalvano.com/compression-tester)
13. Inadequate compression levels
    - The higher the compression level, the more time it takes to compress
    - NGINX (idk what it is but ill check it out)
14. Third parties not compressing 
    - [Third party testing](https://paulcalvano.com/2024-09-03-discovering-third-party-performance-risks/)
    - 4.6K third party domains are serving uncompressed content to users
15. Resize images to webp or avif (Image optimization)
    - sites load images from S3 instead of a CDN (doesn't optimize your images)
16. Gzip compressing images

- Create a hypothesis "This feature will imrpove [metric]"
- Test the feature in dev tools or something
- validate it using RUM or A/B testing
- Monitor it using RUM, performance budget and/or synthetic measurements

# Thinking beyond core web vitals - Anna Migas


# Third party woes - Jason Grigsby


# Reckoning: Frontend's lost decade - Alex Russell
