# Community Discussion Platforms

## Table of Contents
- Personal Advice
- Community is People
- Platform Types: Forum, Chat, Email List
  - Forum Platforms
    - Key Benefits
    - Best Use Cases
  - Chat Platforms
    - Core Features
    - Optimal Scenarios
    - Limitations
  - Email Lists
    - Main Features
    - Ideal Applications
    - Advantages and Challenges
- Community Platform Features and Functionality
  - User-Focused Features
  - Admin-Focused Features
  - Technical Considerations
- Open Source Community Platforms
  - Self-Hosted Solutions
  - Commercially Hosted Open Source
  - Making the Choice
- Table of Platforms
- A Note on Facebook and LinkedIn Groups

## Personal Advice

*(I posted this "personal advice" section to help a small community think through platform options. I've started fleshing out additional details in the subsequent sections. Please share this elsewhere if you think someone will find it useful, along with credit to me and a link back to the canonical URL: <https://peterkaminski.wiki/community_discussion_platforms>. Comments and questions are welcome: <kaminski@istori.com>. By Peter Kaminski. Claude and ChatGPT were used as writing assistants, but I'm responsible for the content. Last updated 2024-11-10.)*

I thought I'd share some platform observations, while noting that a community is not just a tech platform, it's also the people who participate.

Choosing a tech platform goes hand in hand with helping people move to and use the platform. Helping the members use the platform is your primary job. Choosing and operating the tech platform, while very important, must be secondary to humans using the platform.

I currently run both Mattermost and Discourse servers for a couple of communities, and server-wise, they are both easy to set up and maintain. (I could even say "fun", if you're a devops person.)

Server cost for either one runs ~$10 a month on AWS servers; it might be possible to make that a little less on a cheaper VPS provider.

Mattermost is an open source Slack-alike, and it's really nice to use. The IRC / Slack / Mattermost / Discord model, with channels and chat, works great for an active community (daily or near-daily traffic), but it's not great for a low-volume community (traffic once in a while).

With an active chat-based community, you also sort of need a wiki or other knowledgebase to supplement the chat, otherwise good stuff just scrolls away. In a low-volume community, a chat platform feels like a ghost town.

Matrix (primary client is Element, but there are others) is sort of a next-gen IRC, rather than an Slack- or IRC-alike. A small community would kinda fit in there, and even though Matrix is a chat system, it doesn't feel like a ghost town if there's low volume, because you can always join other Matrix channels.

It would be a big change to move the community over to a specialized client, and not everybody would transition over.

Discourse is arguably the best self-hostable forum software. I mean arguably literally, there are a few top contenders, and someone could argue that another one is "best" and not be wrong, based on the community's and maintainer's needs. I have an unsorted list here: [[Open Source Forum Software]]. Not all of those are contenders, but maybe half are.

Discourse is really nice, I like it a lot. However, the default configuration is set up more for a big online community, with probably thousands of people and new people joining every month. Those configuration features actually get in the way of low-volume, small community use.

You can go through and change the configuration of course, but there's a fair bit of that to do, it's a job for a couple people for a week or so part-time.

I highly recommend Discourse for the right-sized community, which is probably north of a dozen participants, with at least a few active every week or so, at least. Unlike chat, the threads (called "topics" in Discourse) don't scroll away as much, and so you can get away using just Discourse for an okay knowledgebase, you don't need a separate wiki or whatever.

Google Groups and Groups.io are also options. Google Groups is free, but it's not my favorite. Last time I needed a mailing list, I opted for Groups.io to avoid being "in the belly of the beast" that is Google. Both can work fine, though, especially if you're looking for a more traditional mailing list-style experience.

Finally, if you're interested in self-hosting a mailing list, GNU Mailman is worth considering. I haven't hosted it personally, but I'm on some Mailman lists, and it seems solid. I can't speak to how much of a lift it is to host, but if anyone's interested, I'm happy to help figure it out—including talking about commercial SMTP providers, if that's of interest.

## Community is People

Communities use tools and processes to interact. In this article, let's talk about community discussion platforms, which are online tools that host people's messages as the people interact with each other.

Your community might be spread across different places, but you still want everyone to feel like they're part of something real.

Maybe your online platform is where everyone hangs out most of the time, or maybe it's just one part of how you connect—alongside video calls or even in-person meetups.

Whatever the case, finding the right platform is about more than just tools; it's about making a place where people feel comfortable to share, support each other, and stay engaged, no matter where they are.

Choosing a tech platform goes hand in hand with helping people move to the platform and to use it. Helping the members use the platform is your primary job. Choosing and operating the tech platform, while very important, must be secondary to humans using the platform.

## Platform Types: Forum, Chat, Email List

Community platforms can be categorized into a couple of types, including 'forum', 'chat', and 'email lists'.

Each approach has its strengths and suits different kinds of community dynamics.

### Forum Platforms

Forum platforms like Discourse, Flarum, or NodeBB excel at organized, threaded discussions that maintain value over time.

#### Key Benefits
- Structured conversations organized by categories
- Rich content organization with tags and categories
- Sophisticated moderation tools
- Custom user roles and permissions
- Comprehensive search functionality
- Member directories and profiles
- Integration capabilities through APIs

#### Best Use Cases
Forums particularly shine when:
- Discussions need to be easily referenced later
- Content needs to be organized hierarchically
- You want conversations to have lasting value
- Community size ranges from dozens to thousands of members
- Discussions happen asynchronously

### Chat Platforms

Chat platforms like Mattermost, Discord, or Matrix focus on real-time communication.

#### Core Features
- Instant messaging capabilities
- Channel-based organization
- Direct messaging and group chats
- Real-time notifications
- Voice and video integration (in some platforms)

#### Optimal Scenarios
Chat works best when:
- Community has daily or near-daily activity
- Quick responses are important
- Real-time collaboration is needed
- You have an active, engaged user base

#### Limitations
However, chat platforms can face certain challenges:
- Can feel empty in low-traffic communities
- Valuable information can quickly scroll away
- May require supplementary knowledge base
- Limited archival capabilities

### Email Lists

Email lists (like GNU Mailman, Google Groups, or Groups.io) provide a traditional, email-centric approach to community discussion.

#### Main Features
- Thread-based conversations delivered to members' inboxes
- Simple subscription/unsubscription management
- Archive access through web interfaces
- Email-based participation (reply to participate)
- Moderation through email commands or web interface
- Digest options for high-volume lists

#### Ideal Applications
Email lists are particularly effective when:
- Members prefer email-based communication
- Participants are less technical or don't want new apps
- Discussions are primarily asynchronous
- You need broad accessibility (email works everywhere)
- Long-form, thoughtful responses are valued
- Historical archives need to be searchable
- You want low technical overhead for setup and maintenance

#### Advantages and Challenges
The email list model has stood the test of time because it leverages a universal communication tool (email) and requires minimal adaptation from users.

However, it lacks some modern community features like rich profiles, real-time interaction, or sophisticated content organization.

Also, email lists can get noisy fast. It can be hard to modulate participation, to keep a balance between productive participation from many members vs. having a few people bloviating.

## Community Platform Features and Functionality

Here are some key features to consider when selecting a community platform, particularly a forum, sorted by user and administrative priorities.

The "Importance" column indicates how critical this feature typically is for most communities.

Remember that feature importance will vary significantly based on your specific community needs and goals. While evaluating platforms, consider both your current requirements and potential future growth—features that seem unnecessary now might become critical as your community evolves.

Be aware that some desired functionality may require additional plugins, custom development, or third-party integrations, which can impact both initial and ongoing costs.

Factor in not just the direct platform costs, but also maintenance, hosting, and potential development expenses.

Finally, don't underestimate the importance of user adoption; the most feature-rich platform won't succeed if it presents too steep a learning curve for your community members.

### User-Focused Features

| Feature              | Description                                     | Importance | Common Pain Points                                |
| -------------------- | ----------------------------------------------- | ---------- | ------------------------------------------------- |
| Mobile Experience    | Responsive design, easy mobile posting/reading  | High       | Poor mobile editors, tiny tap targets             |
| Content Discovery    | Finding relevant posts, search functionality    | High       | Bad search, overwhelming home feeds               |
| Notification Control | Customizable notifications for topics/messages  | High       | Too many notifications, missing important updates |
| Feed Customization   | Ability to follow/unfollow topics or categories | High       | Seeing unwanted content, information overload     |
| Direct Messaging     | Private 1:1 and group messaging                 | High       | Limited DM features, clunky interfaces            |
| Post Editor          | Rich text editing, image uploads, drafts        | High       | Lost drafts, formatting issues, editor bugs       |
| User Profiles        | Customizable profiles, activity history         | Medium     | Limited profile fields, privacy controls          |
| Reading Experience   | Clean layout, dark mode, text sizing            | Medium     | Cluttered design, poor readability                |
| Events System        | Calendar, RSVPs, recurring events               | Medium     | Complex event creation, timezone issues           |

### Admin-Focused Features

| Feature              | Description                          | Importance | Common Pain Points                             |
| -------------------- | ------------------------------------ | ---------- | ---------------------------------------------- |
| Moderation Tools     | Post/user management, content flags  | High       | Limited bulk actions, poor audit trails        |
| User Management      | Roles, permissions, tier management  | High       | Inflexible permission systems                  |
| Analytics            | User engagement, content performance | High       | Limited metrics, poor export options           |
| Content Organization | Categories, tags, pinned posts       | High       | Difficult reorganization, inflexible structure |
| API Access           | Integration capabilities, webhooks   | Medium     | Poor documentation, limited endpoints          |
| Customization        | Theming, branding, layout control    | Medium     | Complex customization, breaking changes        |
| Onboarding Flow      | Welcome process, required fields     | Medium     | Rigid workflows, high drop-off                 |
| Backup/Recovery      | Data export, disaster recovery       | Medium     | Complex backup processes                       |
| Anti-Spam            | Automated protection, captchas       | Medium     | False positives, aggressive filters            |

### Technical Considerations

| Feature      | Description                       | Importance | Common Pain Points                    |
| ------------ | --------------------------------- | ---------- | ------------------------------------- |
| Performance  | Page load times, server resources | High       | Slow searches, heavy pages            |
| Security     | Authentication, data protection   | High       | Complex SSO setup                     |
| Self-Hosting | Server requirements, maintenance  | Medium     | Resource intensive, update management |
| Data Privacy | GDPR compliance, data control     | Medium     | Limited privacy controls              |
| Integration  | Third-party services, SSO         | Medium     | Limited integration options           |

## Open Source Community Platforms

Open source community platforms offer a compelling middle ground between fully commercial services and social media platforms. They provide control and flexibility while respecting user privacy and data ownership.

Let's explore both self-hosted and commercially hosted options:

### Self-Hosted Solutions

Self-hosting open source platforms like Discourse, Flarum, or NodeBB gives you maximum control over your community's infrastructure. You maintain complete data ownership, can customize every aspect of the platform, and aren't subject to unexpected pricing changes or feature removals.

#### Advantages
- Complete control over data and privacy
- Freedom to modify and customize
- No per-user pricing
- Direct access to databases and backups
- Ability to implement custom features
- Control over upgrade timing
- Choice of hosting providers

#### Challenges
- Requires technical expertise to maintain
- Security updates need attention
- Server costs and management
- Initial setup complexity
- Performance tuning responsibility
- Backup management
- Email deliverability setup

#### Costs and Considerations
Typical costs run $5-20/month for hosting on platforms like AWS, DigitalOcean, or Linode, though this can increase with community size and activity.

### Commercially Hosted Open Source

Many open source platforms offer commercial hosting options (like Discourse.org for Discourse). This approach provides many benefits of open source software while eliminating most technical maintenance burden.

#### Advantages
- Professional maintenance and updates
- Managed backups and security
- Technical support available
- Easy setup and onboarding
- Guaranteed uptime and performance
- Email deliverability handled
- Clear upgrade paths

#### Challenges
- Higher monthly costs than self-hosting
- Less direct control over infrastructure
- Potential platform-specific limitations
- May still require technical knowledge for customization
- Usually priced per user/usage

### Making the Choice

Consider these factors when deciding between self-hosted and commercially hosted options:

#### Technical Resources
- Do you have the expertise to manage a server?
- Can you handle security updates and maintenance?
- Are you comfortable with command-line operations?

#### Budget Considerations
- How does your community size affect hosted pricing?
- Can you commit time to server management?
- What's the true cost of technical staff time?

#### Control Requirements
- How important is direct database access?
- Do you need custom modifications?
- Are there specific security or privacy requirements?

#### Growth Plans
- How might costs scale as you grow?
- What technical needs might emerge?
- Will you need migration flexibility?

The beauty of open source solutions is that you can often start with commercial hosting and move to self-hosting later (or vice versa), giving you flexibility as your community's needs evolve.

Many communities begin with commercial hosting to validate their concept, then transition to self-hosting as they grow and develop technical resources.

Either way, choosing an open source platform—whether self-hosted or commercially hosted—means you're investing in a solution that respects your community's independence and privacy while providing the flexibility to adapt as needs change.

## Table of Platforms

| Platform                                                | Type       | OSS?         | Pete | Notes                                                                                                     |
| ------------------------------------------------------- | ---------- | ------------ | ---- | --------------------------------------------------------------------------------------------------------- |
| [Discourse](https://discourse.org)                      | Forum      | open source  | 👍    | Open source, self-hostable ideal for communities with regular activity and at least a dozen participants. |
| [Flarum](https://flarum.org)                            | Forum      | open source  |      | Need more information.                                                                                    |
| [NodeBB](https://nodebb.org)                            | Forum      | open source  |      | Need more information.                                                                                    |
| [MyBB](https://mybb.com)                                | Forum      | open source  |      | Need more information.                                                                                    |
| [phpBB](https://phpbb.com)                              | Forum      | open source  |      | Need more information.                                                                                    |
| [Simple Machines Forum](https://www.simplemachines.org) | Forum      | open source  |      | Need more information.                                                                                    |
| [Lemmy](https://join-lemmy.org)                         | Forum      | open source  |      | Need more information.                                                                                    |
| [Mattermost](https://mattermost.com)                    | Chat       | open source  | 👍    | Open source, self-hostable Slack alternative, best for active communities with frequent interactions.     |
| [Matrix](https://matrix.org)                            | Chat       | open source  | 🙃    | Next-gen IRC platform, Element is the primary client; works for active and low-volume use.                |
| [Groups.io](https://groups.io)                          | Email List | paid service |      | Similar to Google Groups, offering a traditional mailing list experience.                                 |
| [GNU Mailman](https://list.org)                         | Email List | open source  | 👍    | Open source, self-hostable option known for reliable mailing list functionality.                          |
| [Google Groups](https://groups.google.com)              | Email List |              | 😕    | Free, provides traditional mailing list experience.                                                       |

## A Note on Facebook and LinkedIn Groups

While Facebook and LinkedIn groups offer convenient, ready-made platforms for community building, they come with significant trade-offs worth considering.

These platforms provide built-in audiences, familiar interfaces, and zero hosting costs, which can make them attractive options for some communities. Many people already have accounts and know how to use them, eliminating onboarding friction.

However, using these platforms means accepting their fundamental business model: they monetize user attention and data through advertising. Your community's discussions, member information, and engagement patterns become part of their data collection ecosystem.

They can (and do) change features, algorithms, and access rules without warning, potentially disrupting your community's dynamics overnight.

### Key Limitations
- Content ownership and export options are limited
- Discovery is controlled by proprietary algorithms
- Members must have platform accounts to participate
- Privacy controls are subject to platform policies
- Advertising appears throughout discussions
- API access is restricted and can change unexpectedly
- Platform changes are beyond your control

### Considerations for Use
For some communities—particularly those focused on professional networking or casual interest groups—these trade-offs might be acceptable.

However, for communities that value data privacy, content ownership, or long-term stability, self-hosted or independent platforms often prove to be better choices.

The initial investment in setting up your own platform can pay dividends in terms of control, customization, and community independence.

Remember: when you build on someone else's platform, you're subject to their rules, their timeline, and ultimately, their business interests. While this might align with your community's needs, it's important to make this choice consciously rather than defaulting to it out of convenience.
