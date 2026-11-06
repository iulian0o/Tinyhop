# Tinyhop

Tinyhop is a URL shortner that turns long URLs into compact, or read aloud. A whort link is easier to remember and type, 
and it keeps shared content clean. 
Tinyhop focuses on fast reidrects reliable unique links, and handling heavy read traffic.

### Why Tinyhop

Let’s start with what problem Tinyhop solves for me. In the past, when I wanted to share a link to petition for different causes with my followers and friends, 
the URLs were too long for social media platforms. Long URLs are awkward to paste into messages, fit on posters, or read aloud. 
This made the petition harder to see for other people as well. Maybe somebody else had the same problem and I didn’t see the cause for the same reason. 
Tinyhop solves this, not just for me, but for other people too, a struggle with links on social media: different causes with petitions, a blog article, or a small business that wants to promote its website. 
A short link is easier to remember and type, and it keeps shared content clean.

### Tech Stack
- **Backend**: Java + Spring Boot 4 + Maven
- **Frontend**: Angular + Typescript
- **Database**: Redis + In-Memory Java maps (temproray)
- **Infrastructure**: Docker

### Design Notes (Future)
- **Read-heavy optimization**: Redirects will be the hot path, so they will be served
from cache whenever possible
- **Uniqueness**: Short codes and alieases will be checked before they are stored,
so no two links conflict
- **Storage**: In-memory (temporary) keep the initial version simple and fast.
Data does not persist across restats unless persistence is added later